---
layout: default
title: Privacy Policy
lang: en
---

# Veo+ Privacy Policy

**Last updated:** November 25, 2026

*Versão em português: [Política de Privacidade](privacidade.html).*

Veo+ is a desktop application by Vecola Productions that runs **entirely on the
user's own computer**. It turns a topic into a short video narrated with the
user's own voice and, when the user authorizes a YouTube channel, uploads that
video to the user's own channel. Vecola Productions does not operate any server
for Veo+, does not receive any data from the application and has no access to
anything it handles.

## Summary of Google user data

| Question | Answer |
|---|---|
| What Google user data does Veo+ access? | The OAuth token of the channel the user authorizes, and that channel's name, profile picture and ID (scope `youtube.readonly`). With the `youtube.upload` scope it uploads videos and thumbnails; it does not read videos, comments, analytics or data from any other channel. |
| How is the data used? | Only to upload to the user's own channel the videos the user chose to upload, and to show in the interface which channel is connected. It is not used for advertising, profiling, sale, or training AI models. |
| Where is it stored? | Only on the user's computer, inside the Veo+ profile folder. Nothing is sent to Vecola Productions or to any server operated by it. |
| Who is it shared with? | No one. It only travels between the user's computer and Google. |
| How long is it kept and how can it be deleted? | Until the user disconnects the channel (Veo+ revokes the permission with Google and deletes the token) or deletes the profile folder. Access can also be revoked at myaccount.google.com/permissions. |

**Limited Use:** Veo+'s use and transfer to any other app of information
received from Google APIs will adhere to the [Google API Services User Data
Policy][limited-use], including the Limited Use requirements.

## 1. Who controls the data

The user, on their own computer. Whoever installs and runs Veo+ controls the
data the application handles. Vecola Productions does not receive, store or
have access to this data.

## 2. Data the application accesses

**From YouTube, through the API, only for the channel the user authorized:**

| Data | Purpose | Where it is kept |
|---|---|---|
| OAuth access and refresh tokens | Authorize uploading the video and thumbnail | Local file in the profile folder (`perfis/<profile>/credenciais/youtube/`) |
| Channel name, picture and ID | Show in the interface which channel the video goes to | Local file in the profile folder |
| ID and URL of each uploaded video | Upload history of the profile | Local file in the profile folder |

**From the user's computer:** the voice sample the user provides, the topics
the user types, and the scripts, audio, scenes and videos produced.

## 3. OAuth scopes requested

| Scope | Why it is needed |
|---|---|
| `youtube.upload` | Upload the video file and its thumbnail |
| `youtube.readonly` | Read the authorized channel's name and picture to identify it in the interface |

Broader scopes such as `youtube` and `youtube.force-ssl` are **not**
requested.

## 4. Other network requests

- The **AI assistant the user installed and signed in with their own account**
  (Claude Code by Anthropic, or Codex by OpenAI) receives the topic and script
  text to write and review the script, under that provider's terms and privacy
  policy. **No data obtained from the YouTube API is sent to these
  assistants.**
- Components the application needs (for example Python, voice and
  transcription models) are downloaded only after the user confirms.

Voice narration, transcription and 3D rendering run locally; the voice sample
never leaves the computer.

## 5. Revoking access and deleting data

In the application: **Configurações, Canal e publicação, Desconectar canal**
(Settings, Channel and publishing, Disconnect channel). Veo+ revokes the
permission with Google and deletes the token from disk. Deleting the profile
folder removes all remaining data. Independently of the application, access can
be revoked at
[myaccount.google.com/permissions](https://myaccount.google.com/permissions).

## 6. YouTube API Services

Veo+ uses YouTube API Services. By using it, the user agrees to the [YouTube
Terms of Service][yt-terms] and is subject to the [Google Privacy
Policy][google-privacy].

## 7. Contact

Questions or data requests: open an issue at
[github.com/Vecolas/veoplus-politica](https://github.com/Vecolas/veoplus-politica/issues).

© 2026 Vecola Productions. All rights reserved.

[limited-use]: https://developers.google.com/terms/api-services-user-data-policy
[yt-terms]: https://www.youtube.com/t/terms
[google-privacy]: https://policies.google.com/privacy
