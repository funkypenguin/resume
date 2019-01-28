{
    "title":"Microservice-based Cryptocurrency Mining Pools",
    "link":"https://github.com/funkypenguin/cryptonote-nodejs-pool",
    "image":"/img/turtlecoin_mining_pool.png",
    "description":"I started dabbling in mining pools with Docker, and ended up maintaining a popular nodejs application, and a mini-empire of Kubernetes-driven mining pools!",
    "tags":["Docker","Kubernetes","Blockchain","GKE"],
    "weight":"2",
    "featured":true,
    "sitemap": {"priority" : "0.8"}
}

Wanting to learn about blockchain tech by building an NZ mining pool for TurtleCoin, I needed to make several minor adjustments to the nodejs-based mining code, to allow for better operation within Docker Swarm.

I started by contributing a [Dockerfile](https://github.com/turtlecoin/turtle-pool/pull/14) to the repo, with the intention of allowing for future automated builds.

I soon discovered that I needed the pool daemon to [exit if it was unable to start](https://github.com/turtlecoin/turtle-pool/pull/17) the pool for any reason (_so that Docker would detect the exit and recreate the container_)

Finally, for the charts data collection module to generate stats for the charts on the UI, I [added the option to specify the host](https://github.com/turtlecoin/turtle-pool/pull/18) that the _rest_ of the modules expected to use for the API (_originally hardcoded to 127.0.0.1_), since I was running each pool element in a separate container.

Several months later, I ported my mining pool to a [more advanced fork of the original code](https://github.com/dvandal/cryptonote-nodejs-pool), and made some [TurtleCoin-specific modifications](https://github.com/dvandal/cryptonote-nodejs-pool/pulls?utf8=%E2%9C%93&q=is%3Apr+author%3Afunkypenguin), allowing my fork to be used for other TurtleCoin pools. I now [maintain a parallel repo](https://github.com/turtlecoin/funky-turtle-pool) in the TurtleCoin GitHub organisation for this code.

I later moved my pools to Google Kubernetes Engine, both to address limitations of my shared VPS hosting, and to [learn more about Kubernetes](https://geek-cookbook.funkypenguin.co.nz/kubernetes/start/).

I was recently interviewed for the TurtleCoin blog re how my little pool was built, and got to geek out a bit on the microservices aspects - The interview is at https://blog.turtlecoin.lol/archives/funkypenguins-turtle-pool-secrets/
