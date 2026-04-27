# Privacy Policy

Last Updated: 2026-04-15

Cozy Uploader ("the App") values user privacy and complies with applicable data-protection laws including the EU GDPR and the Korean Personal Information Protection Act (PIPA).

---

## 1. Data Controller

- Service Name: Cozy Uploader
- Data Protection Officer: Yoseph Lee
- Contact: cozy_uploader@naver.com
- Official Website: https://cozy-uploader.github.io

## 2. Data We Collect

We only collect the following categories of data. Nothing outside this list is collected.

### 2.1 Account Data (stored on Supabase)
| Item | Purpose | Location |
|------|---------|----------|
| Email address | Authentication, license linking, support | Supabase (EU region, encrypted) |
| Password (hashed) | Login verification | Supabase (bcrypt hash — plaintext never stored) |
| Display name | In-app UI display | Supabase |
| License key / tier / expiry | Paid feature access control | Supabase |

### 2.2 YouTube Integration (stored locally on user PC)
| Item | Purpose | Location |
|------|---------|----------|
| YouTube OAuth Refresh Token | Uploading videos to the user's own channel | %APPDATA%\Cozy Uploader\ |
| Channel ID / Name | Identify target channel, UI display | Local PC |
| Upload history (title / video ID / timestamp) | Prevent duplicates, usage history | Local PC |

Important: YouTube Refresh Tokens and Gemini API keys are never transmitted to or stored on our servers. They reside only on the user's PC.

### 2.3 User-Supplied API Keys (stored locally)
| Item | Purpose | Location |
|------|---------|----------|
| Gemini API Key (user's own) | Calling Google's AI generation APIs | Local PC |
| FFmpeg path and other app settings | Video rendering | Local PC |

## 3. Data We Do Not Collect

- Sensitive personal information (SSN, credit cards, health data)
- YouTube viewer data (e.g., commenters' personal info)
- Third-party channel data
- Location data (GPS or IP-based)
- Telemetry or usage analytics (in the current version)

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
| Account info | 2 years after deactivation/license expiry (for dispute handling) |
| License issuance records | Per Korean E-Commerce Act: 5 years |
| Local PC data | Until the user deletes it themselves |

## 6. Third-Party Services

The App integrates with the following third-party services. Their respective privacy policies apply.

| Service | Purpose | Data Shared | Privacy Policy |
|---------|---------|-------------|----------------|
| Google LLC (YouTube Data API v3) | Uploading to user's own channel | OAuth credentials, video file and metadata | https://policies.google.com/privacy |
| Google LLC (Gemini API) | AI thumbnail / metadata generation | User-entered prompt text | https://policies.google.com/privacy |
| Supabase Inc. | Authentication, license management | Email, password hash, profile | https://supabase.com/privacy |
| Wadiz | Crowdfunding payment processing | Payment / backer data (App does not receive directly) | https://www.wadiz.kr/web/wcomn/policy/privacy |

## 7. Your Rights

Users may exercise the following rights at any time:

- Right to access personal data
- Right to rectification / erasure
- Right to restrict processing
- Right to withdraw (account deletion)

Requests may be sent to cozy_uploader@naver.com. We respond within 10 business days.

Users may revoke YouTube access directly at:
https://myaccount.google.com/permissions

## 8. Security Measures

- Passwords stored using bcrypt hashing — plaintext is never stored
- All Supabase communication over HTTPS / TLS 1.3
- OAuth tokens are stored only on the user's PC and never transmitted to our servers
- Supabase is hosted in the EU region, meeting GDPR-level security standards

## 9. Cookies and Tracking

The App is a desktop application and does not use browser cookies directly. During OAuth sign-in, a browser window opens, at which point Google may use its own cookies.

## 10. Children's Privacy

The App does not knowingly allow users under 14 years of age to register. If data from a user under 14 is identified, it is deleted immediately.

## 11. Changes to This Policy

Material changes will be notified in the App and on the website in advance. Individually significant changes will also be emailed.

## 12. Contact

- Email: cozy_uploader@naver.com
- Korean PIPC Dispute Mediation: https://www.kopico.go.kr (1833-6972)
- Korea Internet & Security Agency: https://privacy.kisa.or.kr (118)

---

This Privacy Policy is effective as of 2026-04-15.
