# Evidence guide: where proof lives in a reproduction package

## Environment

Where it lives: the repro report's environment line; the issue's
stated target version (title, body, or the repo-facts "latest
release" line); any dependency a thread comment names specifically
enough to identify (not a vague "might be a dependency issue").

What good looks like: tool version matches the issue's target, or
states why it differs; any specifically-named implicated dependency
is reported with a version consistent with the thread, or the
difference is explained.

## Steps

Where it lives: the repro report's steps section; any thread evidence
about whether a starting state is required.

What good looks like: each step names a concrete input, command, or
target — not a generic description of an action ("run pytest
tests/foo_test.py", not "run the test suite"). Starting state is
specified when the issue/thread shows it's necessary; genuinely
unknown necessity is a gap in the evidence, not the report's fault.

## Behavior shown

Where it lives: the repro report's artifacts (output excerpts, logs,
screenshots), read against the issue's expected-vs-actual section and
any trigger condition it states.

What good looks like: the artifact demonstrates the issue's specific
trigger condition, not just a symptom that sounds similar under a
different condition. When the issue itself uses a contrast to define
what's special about the trigger (e.g. "with one header, not zero or
two"), the report includes that control — matching words or field
names alone, without the trigger, isn't enough.

## Honesty

Where it lives: the claim comment and repro report's causal language,
and any cannot-reproduce claim, read against the artifacts actually
shown.

What good looks like: certainty in the language matches certainty in
the evidence — hedged claims about unverified causes are fine even
when wrong; asserted causes need artifacts that actually establish
them. A cannot-reproduce claim is only as good as its shown attempt
under the right trigger conditions — a bare assertion isn't evidence.
A genuinely mismatched environment is a separate Environment-check
failure; only a false claim about the environment belongs here.

## Comms

Where it lives: the claim comment and repro report, read against the
issue's specific content; the repo-facts contribution policy's AI-use
line, read against the same comments.

What good looks like: the comment names something unique to this
issue (its symptom, trigger, or the writer's own approach) rather
than generic boilerplate that could apply anywhere. Separately: if
the repo's policy requires AI-use disclosure under some condition,
the comment states it; no stated policy means nothing to check.