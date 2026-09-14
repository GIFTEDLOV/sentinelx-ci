# SentinelX CI evidence publisher

This public repository is the registered CI authority `GIFTEDLOV/sentinelx-ci`.
It is intentionally separate from the SentinelX source repository, but it is
not an independent security publisher. Security evidence must come from a
legitimate publisher whose GitHub owner differs from the source owner.

The workflow checks out an explicitly supplied immutable SentinelX source
commit, retrieves the parent file from an explicitly supplied parent commit,
runs the source repository's deterministic gates, and uploads a CI evidence
envelope as a workflow artifact. It does not deploy, register a target, sign
security evidence, or push generated evidence automatically.

The artifact becomes eligible for a proposal only after an authorized operator
reviews it, publishes it at an immutable commit in this repository, and uses
the exact resulting URL, ID, target, parent hash, candidate hash, and policy
fingerprint.
