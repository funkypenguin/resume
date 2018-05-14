{
    "title":"TurtleCoin Mining Pool Dockerization",
    "link":"https://github.com/turtlecoin/turtle-pool/pulls?utf8=%E2%9C%93&q=is%3Apr+author%3Afunkypenguin+",
    "image":"/img/turtlecoin_mining_pool.png",
    "description":"Several minor PRs against TurtleCoin mining pool to make it Docker-Swarm-Friendly",
    "tags":["Docker"],
    "weight":"999",
    "featured":true,
    "sitemap": {"priority" : "0.8"}
}

Wanting to learn about blockchain tech by building an NZ mining pool for TurtleCoin, I needed to make several minor adjustments to the nodejs-based mining code, to allow for better operation within Docker Swarm.

I contributed a [Dockerfile](https://github.com/turtlecoin/turtle-pool/pull/14) to the repo, with the intention of allowing for future automated builds.

I soon discovered that I needed the pool daemon to [exit if it was unable to start](https://github.com/turtlecoin/turtle-pool/pull/17) the pool for any reason (so that Docker would detect the exit and recreate it.)

Finally, for the charts data collection module to generate stats for the charts on the UI, I needed to [add the option to specify the host](https://github.com/turtlecoin/turtle-pool/pull/18) that the _rest_ of the modules expected to use for the API (_originally hardcoded to 127.0.0.1_)
