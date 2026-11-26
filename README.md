# ForReal

A blunt second opinion for your next idea.

ForReal is a reusable Codex skill that checks your idea against the market, scores it out of 10, and tells you whether to build, test, change direction, or stop. It challenges the proposal without attacking the person behind it.

## What you get

- **Verdict first.** Short, direct reviews, usually 150–250 words.
- **A score out of 10.** A consistent rubric, a component breakdown, and a confidence level.
- **Market checks.** Current competitor comparisons with sources when web access is available. Unverified market judgments are marked provisional.
- **Honest rejection.** If the evidence says the idea is weak, the review says so and explains why.
- **Better directions.** One concrete alternative when the original is weak, with the reason it might work better.
- **A next action.** A practical test or decision, with a clear threshold for continuing or stopping.

It distinguishes an idea that is unoriginal from one that has no competitive advantage. Existing competitors can demonstrate demand; the question is why someone would choose your version.

## Install in Codex

You need Git and Codex with local skill support. Clone this repository into your skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/InshaalAmin-67/ForReal.git "${CODEX_HOME:-$HOME/.codex}/skills/forreal"
```

The destination should not already exist. The repository root contains `SKILL.md`, so it is also the installed skill directory. If you use a different skills location, clone it there with the folder name `forreal`.

## Use

Invoke the skill in Codex:

```text
$forreal Review this idea: a paid habit tracker for university students.
```

Give it your intended audience, budget, available time, and any customer evidence for a more useful assessment:

```text
$forreal I want to build [idea] for [specific users].
They currently use [alternative]. My advantage is [difference].
I have [time/budget/skills]. My evidence so far is [evidence].
Tell me if it deserves my time and what to test first.
```

For a shorter answer:

```text
$forreal Just the score, decisive reason, and next action: [idea]
```

The default response includes a score and verdict, the decisive reasons, a stronger direction when warranted, and one next action. It does not automatically start building the idea or contact potential customers.

## How scoring works

| Dimension | Maximum | What it examines |
| --- | --- | --- |
| Demand | 3 | Evidence that the intended users have the problem and care about solving it. |
| Advantage | 2 | A credible reason to choose this over the closest substitute. |
| Reach | 2 | A realistic way to reach the intended users. |
| Value versus cost | 2 | Whether the likely benefit justifies the cost and effort. |
| Execution | 1 | Whether a useful first version is feasible within the creator's constraints. |
| **Total** | **10** | **The opportunity presented by this version of the idea.** |

- **0–3:** Reject this version.
- **4–5:** Weak; change direction or run only a cheap discriminating test.
- **6–7:** Plausible; validate before substantial implementation.
- **8–10:** Strong enough for the next proportionate commitment, supported by evidence.

The score is a structured judgment, not a success probability. Missing evidence lowers confidence; it is not proof of failure. A fatal dependency can override a favorable total. For content or personal projects, the review uses the stated audience or personal goal rather than assuming profit is required.

## Requirements and portability

ForReal contains instructions and Codex UI metadata. It needs no API key, package installation, or service of its own. Market research relies on the host assistant's available search and browsing tools. Without them, market claims must remain unverified.

Other assistants can use the instructions in [SKILL.md](SKILL.md) as a prompt, but skill discovery and invocation depend on the host. The `$forreal` examples above are for Codex.

## Security

Install from this repository and review changes before updating your installed copy. ForReal is an instruction set: an update can change how your assistant behaves. For a reproducible installation, check out a specific commit you have reviewed rather than automatically following new commits.

Changes to `main` go through pull requests. GitHub Actions is disabled because this project does not need executable workflows. Read [SECURITY.md](SECURITY.md) for the repository safeguards and [report vulnerabilities privately](https://github.com/InshaalAmin-67/ForReal/security/advisories/new).

## Contributing

Open an issue or pull request with the review behavior you want to improve, a realistic example, and why the change would lead to a better decision. Keep reviews concise, preserve the scoring rubric, and require evidence for praise and criticism alike. Use fictional or anonymized examples.

Explain any new tool use, network access, executable files, or permission requirements. Do not include credentials or private customer data in examples. The maintainer reviews contributions before merging; a pull request cannot update the published skill on its own.

## License

[MIT](LICENSE). You may use, modify, and share ForReal under that license.
