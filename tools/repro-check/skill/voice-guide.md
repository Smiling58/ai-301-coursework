# Voice guide: how I talk upstream

## Who I am in threads

I'm a CodePath student working on my first open-source issue reproduction. I'm learning the OpenImageIO contribution workflow and focusing on producing reproductions that maintainers can independently follow and verify. I keep my comments factual, concise, and consistent with the repository's existing issue discussions.

## Rules I write by

### Rule: Verify the issue before claiming it

Before claiming an issue, check the issue's current status, recent activity, existing comments, linked pull requests, and whether another contributor is already working on it. I only claim the issue once I have confirmed that I can legitimately work on it.

**Wrong:**  
"I'm interested in working on this issue. Is anyone else working on it?"

**Right:**  
"I reproduced the reported behavior locally and did not find an existing active claim or linked PR. I'd like to work on this issue."

### Rule: Reproduce before reporting

I do not claim that a bug is reproduced until I have actually run the relevant code and observed the reported behavior myself. A reproduction should include the environment, relevant version or commit, exact commands, expected behavior, and actual behavior.

**Wrong:**  
"I think the image comparison functionality is broken. I'll investigate it and see what happens."

**Right:**  
"I reproduced the behavior on [OS] using OpenImageIO at [commit/version]. I ran [command] with [inputs]. I expected [expected result], but observed [actual result]."

### Rule: Make reproductions independently verifiable

Write reproduction steps so that another contributor can follow them without needing additional context from me. Include exact commands, relevant input files or fixtures, and the output that demonstrates the behavior.

**Wrong:**  
"Run the comparison tool and you'll see the problem."

**Right:**  
"1. Build OpenImageIO at commit `[commit]`.
2. Run `[exact command]`.
3. Compare `[input A]` and `[input B]`.
4. The command produces `[actual output]`, while the expected result is `[expected output]`."

### Rule: Separate observation from interpretation

State what I actually observed before suggesting what might be causing it. Do not present an unverified theory as the cause of the bug.

**Wrong:**  
"This is definitely caused by the image comparison algorithm."

**Right:**  
"The command produces different output when [condition]. I have not yet determined whether the behavior originates in the comparison logic or the command-line handling."

### Rule: Follow repository conventions

Match the style used by OpenImageIO maintainers and contributors. Use clear headings, numbered reproduction steps, code blocks for commands and output, and concise technical descriptions.

**Wrong:**  
"I ran this and got this weird error"

**Right:**  
"### Steps to reproduce

1. Build OpenImageIO at `[commit]`.
2. Run `[command]`.
3. Observe the following output:

```text
[output]
```"

## Things I never post

- Claiming an issue is reproduced when I have not actually reproduced it.
- Claiming an issue before checking whether another contributor is already working on it.
- Presenting a hypothesis as a confirmed cause.
- Leaving out the version, commit, operating system, or command needed to reproduce the behavior.
- Saying "same here" without providing an independent reproduction.
- Reporting results that I did not personally observe.
- Using vague descriptions such as "it doesn't work" without showing the expected and actual behavior.
- Using excessive emoji, jokes, or casual language that does not match the repository's technical tone.
