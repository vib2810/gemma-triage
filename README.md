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

## Assistive apps (new)

Both read the same `gemma-4-E2B-it.litertlm` from your **Downloads** folder (no second copy). After
installing, open the app and tap **Allow access**.

- **Gemma Eyes** ([releases tagged `eyes-v*`](https://github.com/vib2810/gemma-triage/releases?q=eyes&expanded=true)).
  Vision assist for blind and low-vision people: **shake the phone** and it says the biggest hazard
  ahead, then describes the scene. **Ask** a question by voice, **Find** a door or chair with
  left/right guidance, **Read** signs, or turn on **Walk mode**, which speaks only when the view
  changes. It's a description aid, not an obstacle detector.
- **Gemma Memory** ([releases tagged `memory-v*`](https://github.com/vib2810/gemma-triage/releases?q=memory&expanded=true)).
  A memory companion for people who forget. Tap **Remember** and say it in your own words (or add a
  photo); Gemma files it and reads back what it understood. Tap **Ask**: "Where are my keys?" gets the
  answer, when you said it, and your own recording. Reminders, a daily recap, and an **example day**
  in Settings to try it at once. **Family sharing**: give phones the same family code and a caregiver's
  phone sees the memories and can add reminders that ring on every family phone (works without the
  model on the caregiver's phone).

## Lab apps (experiments)

Separate apps that share the same model file. They read `gemma-4-E2B-it.litertlm` straight from your
**Downloads** folder, so there's no second 2.6 GB copy. Install them from their release tags (they are never
"latest", so Gemma Triage's updater ignores them):

- **Gemma Pilot** ([releases tagged `pilot-v*`](https://github.com/vib2810/gemma-triage/releases?q=pilot&expanded=true)).
  Tell the phone what to do ("turn on Do Not Disturb"). Gemma reads the screen and taps through it,
  fully on the phone. After installing: open it, tap **Allow access** (All files access), then
  **Open Accessibility settings → Gemma Pilot → On**. If that switch is greyed out, go to
  *App info → ⋮ → Allow restricted settings* first.
- **Gemma Lens** ([releases tagged `lens-v*`](https://github.com/vib2810/gemma-triage/releases?q=lens&expanded=true)).
  Take or pick a photo and **Ask**, **Point**, **Find all** (boxes), **Read** or **Describe**. Voice questions work too.
  After installing: open it and tap **Allow access**.

If you deleted the model from Downloads after importing it into Gemma Triage, download it again
(the app's **Download** button) and wait until the download finishes.
