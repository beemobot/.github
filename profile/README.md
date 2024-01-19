## Beemo 🐝

Beemo is [Discord](https://discord.com/) Bot dedicated to stopping userbot raids.
It features a powerful algorithm which is fine-tuned for detecting automated user accounts while minimizing false positives as much as possible to not harm real users.

<a href="https://beemo.gg/invite">
    <img src="/res/beemo-profile.png" width="300" height="376">
</a>

Here you can find the components that power Beemo!

- **Tea** is the actual Discord Bot, including the antiraid algorithm and Beemo Max features. It is written in Java and Kotlin and uses the [Javacord](https://github.com/Javacord/Javacord) Discord library. Given Beemo's size (100,000+ Discord Servers), it runs in multiple Clusters, each containing a certain amount of Shards. This part is not open source.
- [**Cafe**](https://github.com/beemobot/cafe) is the Monorepo containing Beemo's open source components. This includes:
   - **Vanilla**, the rate limit coordinator for Tea. Since different Shards of Tea run in different independent Clusters, they have to communicate with Vanilla through [Kafka](https://kafka.apache.org/) to determine which Shard can send how many Discord API requests in a given time frame.
   - **Latte** contains common utilities that is shared between multiple Java/Kotlin components of Beemo.
   - **Milk** serving logs of raids detected by Tea on [logs.beemo.gg](https://logs.beemo.gg/).
- [**beemo.gg**](https://github.com/BeemoBot/beemo.gg) is the source code of, you guessed it, [beemo.gg](https://beemo.gg/)! It automatically gets deployed to Cloudflare Pages once a new commit is pushed.
- [**docs.beemo.gg**](https://github.com/BeemoBot/docs.beemo.gg) similarly contains the source of the [Beemo Documentation](https://docs.beemo.gg/). Those currently use GitHub Pages for deployment.
