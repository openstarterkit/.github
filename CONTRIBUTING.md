# Contributing

Thanks for being here. This project is free and MIT licensed, and it gets better when people who actually use it say what is missing or broken.

Before you spend time on code, please read how contributions are handled here. It is a little different from most repositories, and knowing it up front saves you effort.

## How this repository works

Development happens in a private repository, and each release is published here as a single commit. That keeps the public history clean and readable, and it means the code you see is always a released, working state.

The practical consequence for you: **an accepted pull request is not merged as your commit.** The maintainer reviews it, applies the change upstream, and it ships with the next release. Your contribution is credited in the release notes and in the changelog entry. Nothing is taken silently.

## What is most useful

**Issues and discussions come first.** A clear bug report or a well argued "this is missing" is worth more here than a patch, because it tells us what real users hit. There is no template to fill in: describe what you expected, what happened, and how to reproduce it.

Especially welcome:

- Bugs in the released code, with steps to reproduce
- Security reports, which go through our [security policy](https://github.com/openstarterkit/nextjs-saas-starter-kit/security/policy) and never in a public issue
- Documentation that is wrong, unclear or out of date
- Concrete gaps you hit while shipping your own product with the kit

## Pull requests

They are welcome, with one condition: **open an issue first and wait for a reply**, unless the change is trivial like a typo or a broken link.

**Translations are the standing exception.** From v1.6 the kit ships an i18n scaffold: English complete, and Italian filled in for the documentation, which is there to prove the routing, the switch and the fallback work rather than describe them. The rest of the Italian interface, and every other language, is community driven: send the translation file as a pull request without asking first. There is no scope discussion to have, which is the only thing the issue-first rule exists to protect you from.

This is not bureaucracy. It is a starter kit, so every feature added becomes code that thousands of people would carry into their own products and maintain forever. That makes the bar for inclusion high, and it is a bar about scope and direction, not about the quality of your work.

Please also know, plainly: **every contribution is reviewed, and it may be declined.** A pull request being open is not a commitment to accept it. If we decline one we will say why, and it is usually one of these reasons:

- It belongs in a specific product rather than in a generic starter
- It adds a dependency where the kit deliberately stays lean
- It locks users into a vendor, which is the one thing this kit exists to avoid
- It duplicates something already solvable with the existing pieces

If you would rather not work under those terms, that is completely fair. The license is MIT: fork it and build what you want, with no obligation to us.

## If you do send a patch

Keep it focused on one thing, and make sure `npm run lint`, `npx tsc --noEmit` and `npm test` pass. Match the style already in the file you are editing. Explain in the description what problem it solves, not only what the code does.

## Roadmap and direction

The [roadmap](https://github.com/openstarterkit/nextjs-saas-starter-kit/blob/main/ROADMAP.md) is indicative and can be reordered based on what people ask for. If something on it matters to you, say so in an issue. That signal genuinely changes the order.

## Versioning

The kit follows [Semantic Versioning](https://semver.org/), with one clarification that matters for a starter kit: there is no package to install, so the public API is not a set of exported functions. It is what we promise to people who already cloned the kit and want to pull an update.

That turns every release into one question, with a testable answer:

**What does someone who already cloned have to do, to take this version?**

- **Patch** (1.5.0 to 1.5.1). `git pull` is enough. Fixes and maintenance, no new features.
- **Minor** (1.5.0 to 1.6.0). `git pull` and `npm install`, at most a migration that runs on its own or a new optional environment variable. Things are added, nothing is taken away.
- **Major** (1.x to 2.0.0). You have to do something by hand: a newly required environment variable, a migration to review against your own data, a renamed file you were told to edit, a higher runtime, or a feature removed.

Note that this does not track how much work went into a release. A release can take two weeks and still be a minor; renaming one environment variable takes ten minutes and is a major.

Dependency updates do not get a version of their own. They ride along with whatever release ships next, unless a security advisory is critical, has a real fix available, and affects the runtime. In that case a patch ships on its own, as [1.4.1](https://github.com/openstarterkit/nextjs-saas-starter-kit/blob/main/CHANGELOG.md) did.

The changelog format follows [Keep a Changelog](https://keepachangelog.com/).

## Code of conduct

Be decent. Assume the other person is trying to help, and disagree about the work rather than the person. Behaviour that makes this a worse place to be will be moderated.

The formal version, which is the one that applies if it ever has to be enforced, is in [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md).
