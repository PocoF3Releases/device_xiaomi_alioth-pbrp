# Final patch series

Apply once to clean sibling repositories using `git am`, in filename order.
Do not apply to the already-patched development checkout.

| Directory | Repository | Baseline |
|---|---|---|
| recovery | bootable/recovery | 4ea56986534da92b29c73ea1907e10e3c0d5ef50 |
| vendor-pb | vendor/pb | 2124e85c72c4d4ff9ef18a7303950d0480257e34 |
| system-sepolicy | system/sepolicy | dd91f58a018a43d70c40abb86dddb85368015b96 |

Recovery patches 0001–0005 retain TeamWin contributors' authorship.
0006 contains the final Alioth adaptation, including GUI/frame pacing,
Magisk fallback, supported partitions and both active-slot ramdisk installers.
The recovery series was replayed from its baseline and its final Git tree
matched the built source exactly. Superseded Alioth patches are removed.

The vendor patch allows recovery adbd to change context. The system policy
patch permits only PBRP's seven upstream permissive recovery service domains
in user recovery builds. Android policy and neverallow checks stay enabled.
