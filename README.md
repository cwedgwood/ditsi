# ditsi

## Name

<ins>D</ins>iminished <ins>i</ins>SCSI-<ins>T</ins>arget <ins>S</ins>torage <ins>I</ins>nterface

Names are hard.

Diminished, diminutive or dumb?  IDK, woke world.

## Justification

Many vendor-provided CSIs are large, closed-source, very complicated
and difficult to debug.

The plan is to write a minimalist CSI that works for my personal needs
then extend to see if it can talk to vendor appliances; initially this
means iSCSI as provided by LIO, ZFS Zvols and iSCSI with multipath
support.

If nothing else it might help me gain an appreciate for why storage
vendors have such large complicated stacks to do something which seems
simple.  Hubris is a thing. Lack of it more so.

NiH also a thing.

The reality is that I might not update this for fivever and this will
just remain and idea.

## Goals

No CRDs.  No CRs.  BecauseReasons.  It makes things easier.

Use as many existing (core) k8s API objects as possible, secrets and
configmaps should be minimalist.

Avoid too many leaky abstractions.  Some vendor deployments have k8s
object interface features in their high-level configuration, that
seems like a bad idea.
