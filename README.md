# Yapper models

Public files for the [Yapper](https://yapper.ca) audiobook and podcast app. The app reads them; there is nothing to install from here by hand.

- `models.v1.json`: the list of voice models Yapper offers and the engines that run them.
- `models.v1.json.sig`: its Ed25519 signature. The app refuses a list whose signature does not verify under a key built into the app, or that is older than the list it has.
- Release `engine-packs`: engine pack archives, Yapper's own small engine programs. Each archive holds a signed manifest, and the signed list gives its SHA-256. The Python packages a pack needs come from the Python Package Index at install, each checked against a pinned hash.

No model weights are stored here. The app downloads models from Hugging Face, at pinned commits with checked digests, after the user accepts each model's license.

The app's source is kept in a separate repository. Changes here are made by Yapper's release process; a hand-edited file will not verify.
