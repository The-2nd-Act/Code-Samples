# The 2nd Act: Code Samples

Companion code, templates, and downloadable files for posts published on **The 2nd Act**, a Substack by Thomas Jochim on building companies in the AI era.

Everything here is meant to be read, copied, and adapted. When a post references a working template, script, or config, this is where the full, sanitized version lives.

Read the publication: https://the2act.substack.com/p/my-second-act-what-30-years-in-enterprise

> Replace the link above with your live Substack URL.

## How this repo is organized

One folder per post. Each folder is named with a short slug, is self-contained, and carries its own README that explains the files and links back to the post they came from. You can grab a single folder without needing anything else in the repo.

```
.
├── open-brain-output-templates/      Companion files for "From Capture to Clarity"
│   ├── README.md
│   ├── daily_brief_template.html
│   ├── weekly_digest_template.html
│   └── monthly_summary_template.html
├── LICENSE
└── README.md
```

## Index

| Post | Folder | What's inside |
| --- | --- | --- |
| From Capture to Clarity: Building Automated Intelligence Reports from Your Open Brain | [`open-brain-output-templates`](open-brain-output-templates) | Three self-contained HTML report templates (Daily Brief, Weekly Digest, Monthly Executive Summary) |

More folders are added here as new posts ship. If a post you're reading references code that isn't listed yet, check back shortly or open an issue.

## Using the samples

You can pull the whole repo or just the piece you need. To clone everything:

```bash
git clone REPLACE_WITH_REPO_URL
```

To grab a single file, open it on GitHub and use the download or raw option. Most samples are static assets (HTML, JSON, config snippets), so in many cases you can open a file directly in a browser or paste it straight into your own project. Each folder's README covers anything specific to that sample.

## A note on sanitization and security

Every sample here is genericized on purpose. Business-specific names are replaced with generic labels, people are replaced with roles, and no keys, tokens, project references, or internal URLs are included. When you adapt a sample for your own use, keep your real secrets out of version control: use environment variables or a local config file that is listed in `.gitignore`, and never commit an API key or endpoint you would not want public. If something looks like a placeholder, it is meant to be replaced.

## Issues and feedback

Found a bug, a broken link, or something that could be clearer? Open an issue on this repo, or leave a comment on the post it relates to. Suggestions and improvements are welcome.

## License

Released under the MIT License. Copy, adapt, and build on any of it, in personal or commercial projects. See [LICENSE](LICENSE) for the full terms.

## About

The 2nd Act is written by Thomas Jochim, covering the practical work of building companies in the AI era: the infrastructure, the tooling, and the systems behind the scenes. This repo is the code companion to those posts.

If the samples are useful, consider [subscribing] https://the2act.substack.com/ so you catch the next one.
