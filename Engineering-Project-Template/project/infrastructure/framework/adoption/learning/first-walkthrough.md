# A first infrastructure design in an afternoon

## Goal

Design a place to keep a nightly survey export. Practice on paper or in a disposable environment you control. The producer is a scheduled job. The consumer is the analyst who must read yesterday's export in the morning.

1. Draw four boxes for the producer, its credential issuer, the storage endpoint and the reader. Draw a second path for recovering the file. Mark each network and identity boundary. Ask who supplies the endpoint name, time and encryption key.
2. Write down the promise in the reader's terms. For this exercise, the 02:00 export must be readable by 07:00, and the previous seven exports must each be retrievable. Record the time zone. Choose a synthetic export with a date, row count and known digest.
3. Give the producer permission to create that day's version. Give the reader access to completed versions. Identify who can delete or restore a version. Predict the results of a successful read, an unauthorized deletion and an expired producer credential.
4. Trace an accidental overwrite. Locate the earlier version, restore it under a different name, verify the row count and digest, and ask the reader to open it. If one operator can destroy every retained version, trace recovery after loss of that account.
5. Estimate retained bytes from export size and version count. Add separate recovery copies, temporary restore space and growth. Hand the drawing to another engineer and ask them to find yesterday's export.

Distinguish predictions from observations in your notes. Mark restore duration as unmeasured until someone times the read from a restored copy. Transfer accepted needs to the [project brief](../../records/intake/project-brief.md).
