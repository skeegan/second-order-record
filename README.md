# The Record

The public prediction record of **Second Order**, a channel about the second-order effects of technology.
Every prediction made on the channel is written here before or when its episode is published, with a date, a
probability, and the rule that will decide whether it came true.

## Rules

1. **Append only.** An entry is never edited or deleted. A clarification, a correction or a score is a new entry that names
   the entry it refers to.
2. **Decided in advance.** Every prediction states how it will be resolved and from which source, before the outcome is known.
3. **Scored in public.** When the due date passes, the prediction is scored RIGHT, WRONG or VOID (if the source no longer
   exists or the question became meaningless), with a link to the evidence.
4. **Provable dates.** The git history is public and the commits are signed. Each version of `record.jsonl` is stamped with
   OpenTimestamps (`record.jsonl.ots`), which anchors a fingerprint of the file in the Bitcoin blockchain, so anyone can verify
   that these words existed on the stated date without trusting the author or the host.

## Files

- `record.jsonl`: the record, one JSON entry per line, in the order written.
- `record.jsonl.ots`: the OpenTimestamps proof for the current `record.jsonl`. Verify with `ots verify record.jsonl.ots`.
- `HASHES.txt`: the SHA-256 of each entry line, so a single entry can be checked on its own.

## Reading an entry

`id` is the episode and the letter. `p` is the stated probability that the claim is true. `resolves_by` is the last date on
which evidence counts. `status` is `open` until a later `score` entry refers to it.
