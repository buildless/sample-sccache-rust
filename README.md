# rust + redis sample

[Buildless][1], [Rust][2], [Redis][3] and [Sccache][4].


## Details about this sample

Together, these tools provide a Rust development environment, enabled with blazing-fast remote build caching. Buildless handles build caching for the app.


### Additional resources

- [Buildless docs: Redis setup][4]


## Trying the sample

> **Before you start:** Obtain an API key for [Buildless][1], set it at `BUILDLESS_APIKEY` in your environment
> Install [Sccache][4]
> Create an environment variable `RUSTC_WRAPPER` and set it to `sccache`
> Create an environment variable `SCCACHE_REDIS` and set it to `rediss://apikey:{YOUR_KEY}@redis.less.build:6379`

1) Clone the sample
2) Run a build with `cargo build`; observe that Rust uses Buildless

That's it! Enjoy lightning-fast builds on Rust 🔥


### Building and running the app

> To build the Rust app:
```
cargo build --all
```

> To run the Rust app:
```
cargo run
```


## Using the sample for your own codebase

This is a [GitHub Template repository][6]; you can easily use it to create your own repo. Follow these steps to customize it
for use with your Buildless account:

1) Update `.github/CODEOWNERS`
2) Add a [GitHub Secret][7] called `BUILDLESS_APIKEY`, set to the API key you want to use in CI
3) That's it!


### Sharing an API key across an organization

You can use [Organization Secrets][8] to automatically provide a `BUILDLESS_APIKEY` to all your repos.


[1]: https://less.build/
[2]: https://www.rust-lang.org/
[3]: https://redis.io/
[4]: https://github.com/mozilla/sccache
[5]: https://docs.less.build/docs/redis
[6]: https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template
[7]: https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions
[8]: https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions#creating-secrets-for-an-organization