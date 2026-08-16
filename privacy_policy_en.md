# Privacy Policy

**Last Updated: 2026-08-15**

> **2026-08-12 correction**: The previous version stated that data is stored in the **EU region**. The actual storage location is the **Republic of Korea (Seoul region)**. This has been corrected. See the Korean version for the authoritative text.

Cozy Uploader ("the App") values user privacy and complies with the Korean Personal Information Protection Act (PIPA).

**This service is offered to residents of the Republic of Korea.** Data is stored in the Republic of Korea (Seoul region). This English text is provided for review purposes; **the Korean version prevails** in case of any discrepancy.

---

## 1. Data Controller

- Service Name: **Cozy Uploader**
- Data Protection Officer: Yoseph Lee
- Contact: **cozy_uploader@naver.com**
- Official Website: https://cozyuploader.github.io

## 2. Data We Collect

We only collect the following categories of data. Nothing outside this list is collected.

### 2.1 Account Data (stored on Supabase)
| Item | Purpose | Location |
|------|---------|----------|
| Email address | Authentication, license linking, support | Supabase (**Seoul region, Republic of Korea**, encrypted) |
| Password (hashed) | Login verification | Supabase (bcrypt hash — plaintext never stored) |
| Display name | In-app UI display | Supabase |
| License key / tier / expiry | Paid feature access control | Supabase |

### 2.2 YouTube Integration (stored locally on user PC)
| Item | Purpose | Location |
|------|---------|----------|
| **YouTube OAuth Refresh Token** | Uploading videos to the user's own channel | **Windows Credential Manager** (entry name `CozyUploader`) |
| Channel ID / Name | Identify target channel, UI display | `C:\Users\<user>\.cozy-uploader\` |
| Upload history (title / video ID / timestamp) | Prevent duplicates, usage history | 〃 |

**Important**: YouTube Refresh Tokens and Gemini API keys are **never transmitted to or stored on our servers**. They reside only on the user's PC.

### 2.3 User-Supplied API Keys (stored locally)
| Item | Purpose | Location |
|------|---------|----------|
| **Gemini API Key (user's own)** | Calling Google's AI generation APIs | **Windows Credential Manager** |
| FFmpeg path and other app settings | Video rendering | `C:\Users\<user>\.cozy-uploader\` |

**How to delete local data.** Tokens and API keys are **not stored as files**. They are
kept in the Windows Credential Manager under the name `CozyUploader`. The
`youtube_cred_*.json` files inside the app folder are only markers indicating that the
real value lives in the Credential Manager. To remove everything from your PC you must
therefore clear **two** places: the folder `C:\Users\<user>\.cozy-uploader\` and the
`CozyUploader` entries in the Credential Manager. If "start with Windows" was enabled,
the registry value `HKCU\Software\Microsoft\Windows\CurrentVersion\Run\CozyUploader`
is removed automatically on uninstall from version 1.3.11 onward.

Older versions also recorded the FFmpeg location under the registry key
`HKCU\Software\CozyUploader`. That value contains an install path and may therefore
include your Windows account name. The current version does not use this key, and it is
removed automatically on uninstall from version 1.3.12 onward. If you uninstalled an
earlier version, the key may still be present and can be deleted manually.

> **Correction (2026-08-14)**: earlier versions of this policy stated these items were
> stored in `%APPDATA%\Cozy Uploader\`. That folder does not exist; the actual locations
> are as listed above.

> **Authoritative text**: this English page is a courtesy translation.
> The Korean version (`privacy_policy_ko`) is the authoritative text and
> prevails in case of any discrepancy.

## 3. Data We Do Not Collect

- Sensitive personal information (SSN, credit cards, health data)
- YouTube viewer data (e.g., commenters' personal info)
- Third-party channel data
- Location data (GPS or IP-based)
- Advertising identifiers or behavioural tracking technologies

> **Correction (2026-08-15)**: an earlier version of this page listed
> "Telemetry or usage analytics" here. That was inaccurate. The app **can**
> send usage telemetry and crash reports, but **only if you switch them on** —
> both are **off by default**. See section 2.3 and the Korean policy
> (which is the authoritative text) for details.

## 4. Purpose of Processing

Collected data is used only for the following purposes. Any change of purpose will be notified in advance.

1. User registration and authentication
2. License key issuance, management, and expiry checks
3. Providing the YouTube video upload feature (user's own channel only)
4. Providing AI generation features (using the user's own Gemini API key)
5. Responding to support inquiries

## 5. Retention Period

| Category | Retention |
|----------|-----------|
| Account info | **2 years** after deactivation/license expiry (for dispute handling) |
| License issuance records | Per Korean E-Commerce Act: **5 years** |
| Local PC data | Until the user deletes it themselves |

## 6. Third-Party Services

The App integrates with the following third-party services. Their respective privacy policies apply.

| Service | Purpose | Data Shared | Privacy Policy |
|---------|---------|-------------|----------------|
| **Google LLC (YouTube Data API v3)** | Uploading to user's own channel | OAuth credentials, video file and metadata | https://policies.google.com/privacy |
| **Google LLC (Gemini API)** | AI thumbnail / metadata generation | User-entered prompt text | https://policies.google.com/privacy |
| **Supabase Inc.** | Authentication, license management | Email, password hash, profile | https://supabase.com/privacy |
| **Wadiz** | Crowdfunding payment processing | Payment / backer data (App does not receive directly) | https://www.wadiz.kr/web/wcomn/policy/privacy |
| **OpenAI, L.L.C.** *(optional)* | Thumbnail image generation, when the user selects the OpenAI engine | User-entered prompt text | https://openai.com/policies/privacy-policy |
| **Kakao Corp.** *(optional)* | Upload completion notifications, when the user connects Kakao | Kakao account credentials, notification text | https://www.kakao.com/policy/privacy |
| **Functional Software, Inc. (Sentry)** *(optional)* | Crash diagnostics, when the user opts in | Error location and app state. Email address, account name, IP address, passwords and tokens are stripped — **but the Windows account name that appears inside error messages and internal file paths is not masked** (see the correction below) | https://sentry.io/privacy/ |

> **Optional services are off by default.** Nothing is sent to OpenAI, Kakao or
> Sentry unless you enable them in Settings.

> **Correction (2026-08-15) — path masking.** Error reports sent to our own server
> (`error_logs`) and uploaded log files have the Windows account name in file paths
> replaced with `\Users\***\`. Two limits apply, and the earlier text did not say so:
> masking ships **from version 1.3.12 onward** (it is not present in 1.3.8, the version
> currently published), and it is **not applied to crash reports sent to Sentry**.
> If you do not want your Windows account name to leave your PC, keep the
> "send diagnostic information" setting switched off.

## 7. Your Rights

Users may exercise the following rights at any time:

- Right to **access** personal data
- Right to **rectification / erasure**
- Right to **restrict processing**
- Right to **withdraw** (account deletion)

Requests may be sent to `cozy_uploader@naver.com`. We respond within **10 business days**.

Users may revoke YouTube access directly at:
https://myaccount.google.com/permissions

## 8. Security Measures

- Passwords stored using **bcrypt hashing** — plaintext is never stored
- All Supabase communication over **HTTPS / TLS 1.3**
- OAuth tokens are stored only on the user's PC and never transmitted to our servers
- Supabase data is hosted in the **Seoul region (Republic of Korea)**

## 8.1 Breach Notification

If we become aware that personal data has been breached, we (1) act immediately to
contain the breach, (2) notify affected users by email **without delay and within 72
hours**, stating the data items involved, when and how the breach occurred, what you
can do, what we have done, and a contact for enquiries, and (3) report the breach to
the Korean Personal Information Protection Commission or KISA where the law requires
it. If we cannot reach you, we post the notice on https://cozyuploader.github.io for
at least 30 days. (PIPA Article 34)

## 9. Cookies and Tracking

The App is a desktop application and does not use browser cookies directly. During OAuth sign-in, a browser window opens, at which point Google may use its own cookies.

## 10. Children's Privacy

The App does not knowingly allow users under **14 years of age** to register. If data from a user under 14 is identified, it is deleted immediately.

## 11. Changes to This Policy

Material changes will be notified in the App and on the website in advance. Individually significant changes will also be emailed.

## 12. Contact

- Email: **cozy_uploader@naver.com**
- Korean PIPC Dispute Mediation: https://www.kopico.go.kr (1833-6972)
- Korea Internet & Security Agency: https://privacy.kisa.or.kr (118)

---

**This Privacy Policy is effective as of 2026-08-15.**
