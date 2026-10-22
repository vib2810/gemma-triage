# Gemma Triage

Voice-to-triage-tag on your phone, made by **Gemma 4 running entirely on the device**: no internet,
no cloud, no account. Phones running the app find each other over Bluetooth/Wi-Fi and share every tag
automatically. Built for the Google Gemma Hardware Hackathon (AGI House, Oct 24 2026).

## Install (Android 12+, 64-bit ARM phone)

1. On the phone, open **[Releases → latest](https://github.com/vib2810/gemma-triage/releases/latest)**
   and tap the `gemma-triage-*.apk` file. Open it and tap **Install**
   (allow "install unknown apps" for your browser; on Samsung, turn off
   *Settings → Security and privacy → Auto Blocker* if the install is blocked).
2. Open **Gemma Triage** and allow every permission (microphone, camera, nearby devices, location;
   the last two are what phone-to-phone sync needs).
3. **Get the model once** (2.6 GB, use Wi-Fi): tap **Download model in browser**. When the download
   finishes, go to **Team → Import model file** and pick `gemma-4-E2B-it.litertlm` from Downloads.
   The app copies it in; you can then delete the downloaded copy.

> Updating the app keeps the model. **Uninstalling deletes it**, so update instead of reinstalling.

## Updates

The app updates itself. At launch it checks this page; on Wi-Fi it downloads a new version in the
background and shows **Update x.y ready · Install** on the Board. The first time, Android asks you to
allow "install unknown apps" for Gemma Triage and to confirm; later updates install with one tap.
Tags and the model are kept. You can turn checking off in **Team → App updates**.

## Using it

- **Tag patient**: hold the big mic button, describe the patient (injuries, breathing, pulse,
  responds?, walking?, where), release. Gemma fills a START triage tag in a few seconds and reads it
  back. Fix the color if needed, then **Save & share**. A photo or typed note can be added.
- **Board**: counts by color (tap to filter), every patient from every phone, "updated x ago".
  Tap a patient to re-tag, mark transported, or delete.
- **Team**: nearby phones and sync status, rename this phone (e.g. "Medic 1"), model and backend.

The model is [Gemma 4 E2B (LiteRT-LM)](https://huggingface.co/litert-community/gemma-4-E2B-it-litert-lm),
Apache-2.0. Gemma and phone-to-phone sync never use the internet; the only network use is the update check.
