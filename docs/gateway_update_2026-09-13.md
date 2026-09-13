# Research gateway update — 2026-09-13

## Reason and scope

The remote main at `07f20eb5bbea1e49d0b5f60fc4962c45ddcd3704` routed new readers mainly to V8/V9, while local papers and public DOI registrations extended through V14. Several guides still said DOI pending or pre-release, the timeline incorrectly reported V14's local PDF absent, and old SSOT labels could be read as current series-wide authority.

The documentation update supplies an interest-based entry, a V4–V14 paper/edition/status map, formal citations, V12 and V13 implementation/result paths, one bounded demo explanation, and scoped historical anchors. It aligns the related notes guides, timeline, and CFF references. The GitHub About description should be aligned after merge; its previous text was `Public gateway for the Decision-OS series (V4–V9). Canonical artifacts on Zenodo (DOI).`

This is navigation work. It does not change paper bodies, PDFs, evidence, hashes, release/tag objects, software, dependencies, workflow logic, or control rules. Existing artifacts retain their filenames and locations.

## Baseline and local isolation

- Remote main: `07f20eb5bbea1e49d0b5f60fc4962c45ddcd3704`, confirmed by fetch, `ls-remote`, and GitHub API.
- Work branch: `codex/research-entry-20260913`, in a new dedicated checkout. Existing workspace repositories and untracked work were left untouched.
- The macOS checkout initially displayed one Unicode-normalized SVG as untracked. Setting this checkout's `core.precomposeunicode=false` restored clean status without editing, moving, or renaming that tracked artifact.
- No applicable ancestor or repository `AGENTS.md` was found. The repository's existing PR template is What / Why / Risk or externality / Evidence.
- At baseline the GitHub API reported `main` unprotected, no applicable rules, no required review/status contexts, no open PRs, and merge commits enabled. Settings are rechecked on the PR before merge; no protection bypass is authorized or used.

## Source verification

The [publication timeline](research_timeline.md#publication-sequence) links all 32 selected version DOI registrations. They were fetched directly from `api.datacite.org/dois/10.5281/zenodo.<record>` on 2026-09-13, together with five concept registrations used to resolve V6/V7/V8/V9/V10 relationships. All 37 records returned findable metadata. Registered titles, version labels, resource types, Issued dates, related identifiers, and relevant abstracts were inspected.

This is publisher-supplied DOI registration evidence, not a re-use of the timeline's previous verification labels. Direct requests to Zenodo landing pages and API timed out; failed fetches are recorded as inaccessible, not broken links. We do not claim a fresh Zenodo download or a byte comparison against the local PDFs.

Local primary reading was targeted to the claims needed for routing: covers/abstracts and relevant scope sections of V4, V5 Revised, V6 commitment, V7 Final, V8, V9.1, V10 Note/full, V11 Note/full, V12 v2, V13 v0.2, and V14, plus the V6 one-page verification proposal. V14's cover was also visually inspected. The V10/V11 precursor titles and content agree with their own registrations; they were not assigned the later Full Paper DOI.

Key corrections supported by those sources:

- V6 local `v2` corresponds by title/content to the commitment paper registered as version `V4`; its record explicitly names the earlier PIC DOI as a prior version. The filename was not changed and byte identity is not asserted.
- V7 Final English is publicly registered and present locally; the Japanese source-state master remains a separate artifact. The shared concept relation is established; “Final” does not establish peer review or sufficient AGI conditions.
- V10 Full Paper is deposited `v2.0`, despite local `_v1` filenames. Its earlier Note has DOI `19871495`; V11's earlier Note has DOI `19872064`.
- V12 v2 is a public preprint with a separately linked software companion. Its fresh-evaluation proposal is not equated with complete implementation in the CLI.
- V13 v0.1 has DOI `20604577`; v0.2 is a public Research Note / Prototype-Bound Draft, not a finished v1.0 paper.
- V14 v0.1 has DOI `21148211` and a local PDF. Its registered scope excludes a full implementation architecture and empirical benchmark.
- Registered multiple Issued dates are exposed in the timeline; no date field or external metadata was rewritten.

## Implementation evidence inspected

| Source | Inspected identity and evidence | Limit |
| --- | --- | --- |
| V12 Completion Integrity | Public main `be1b3f70128d67e642d288c2bab9b53719720c37`; README, CLI/validator, workflow, examples guide; [CI run 27920845535](https://github.com/shin4141/decision-os-v12-completion-integrity/actions/runs/27920845535) returned success | Nine example-record checks establish structural/output agreement, not source truth, code correctness, or complete paper validation. Existing CI was inspected, not relabeled as a new experimental trial. |
| V13 LoopKit | Public main `42e406e858b05b6b8aff5cc6669cf10ad506b424`; README, onboarding, reading order, prototype status, Forward Use 003/004, Runner external validation, onboarding validation, Cycle 006 terminal failure | Creator-owned/internal bounded records. One private-target patch is not independent public replication; scanner usefulness is mixed; onboarding record leaves a public-URL trial open; Cycle 006 establishes a failure boundary only and the file remains marked draft. See the [fixed record links](../README.md#public-implementations-and-evidence). |
| MMAR/L0 and SiriusA | MMAR public main `3b7261d75f6b6c9ec55ad07268a3540ca36d7a36`, README and schema paths; SiriusA README; this gateway's existing workflow source | The gateway imports the moving MMAR main and adds synthetic policy annotations. It does not test full V5 Revised mechanisms or live risk detection. Root schema paths replace the old nonexistent `schema/` routes. |

Software releases V12 `v2.2.3` and V13 `v0.1.0` were inspected separately from current main and paper deposits. No software release or tag was changed.

## Validation and review

Completed before the initial commit:

- Source-to-description and documentation diff review, plus `git diff --check`: passed.
- Markdown parsing across 21 changed Markdown files: 216 internal links and 41 anchor targets passed; unchanged guides were also checked for inbound links to removed headings.
- CFF 1.2.0 validated against the official citation-file-format schema; all 21 reference titles, versions, and years match the corresponding primary DOI registrations.
- All 66 original non-document files were compared byte-for-byte with the baseline, including PDFs, evidence, workflow, images, and thresholds: unchanged.
- Major external GitHub paths, public repository status, releases, workflow/run identities, and schema locations were verified by API. The 92 distinct external URLs in changed Markdown were classified separately as reachable endpoints or DOI/registration-backed references with unverified Zenodo destinations.
- Seven primary guides were rendered by GitHub's Markdown API; tables and heading text were inspected. This API does not emit heading anchor IDs, so anchor paths were checked separately and are rechecked on the published page.

The PR and workflow run links are recorded in the PR using the existing template. The existing Decision Gate workflow is the only repository workflow; it triggers on main push and manual dispatch, not PR events. A manual `pass` run on the work branch is used before merge, followed by the normal main-push run.

Reader-path review starts at README and follows: a current paper → formal DOI; an interest → local guide; V12/V13 → public code; and implementation → fixed result plus limits. The PR must distinguish Codex's diff/source review from an independent peer review or externally approved scientific claim. If no mandatory reviewers/checks are configured, that fact is recorded rather than an approval being invented.

## Remaining uncertainty

- Direct Zenodo landing-page/file access and local/deposit byte identity were not verified; historical partial hashes and PDF/commit associations remain historical only.
- No peer-review outcome, complete-theory empirical validation, universal performance benefit, or independent reproduction of the selected V13 cases was established.
- Metadata retains ambiguous historical dates and the V6 addendum's old local path. Existing V9.1 lock metadata remains unspecified; old listed `fig/` paths are absent.
- A V13 v1.0 final paper was not verified. The software's later features and internal records do not change the publication status of the research note.

## Rollback and restart

The merge is required to use a merge commit so both parents and branch history remain inspectable. Revert that merge with `git revert -m 1 <merge-commit>` through the normal PR path; do not reset or force-push main. The PR records the actual merge SHA and remote read-back. Reverting this documentation merge restores prior navigation without altering any paper, evidence, release, or tag. If the About description was aligned, restore the exact prior description quoted above separately.

For a future update, fetch current remote main, read the relevant DOI registrations and narrowly selected implementation records, and amend the current guides plus this repository's timeline/PR record. An old successful record must remain scoped to its original commit, inputs, and limits.
