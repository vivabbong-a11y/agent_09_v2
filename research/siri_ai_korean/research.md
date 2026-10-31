# Siri AI in Korean (iOS 27.2) — Research Notes

- Date: 2026-10-31
- Scope: A practical, source-checked basis for a Naver blog guide to using **Siri AI** (Apple's new Apple Intelligence-based Siri) in Korean. It covers what changed from the old Siri, how to turn it on, what works in Korean now (with example commands), limits, privacy, the paid tier and FAQs. Facts come from Apple's own pages (Newsroom, Support) where they were reachable, with Korean and English media as cross-checks. Every example command is marked **documented** (Apple or the press describes that scenario) or **inferred** (our own wording of a documented capability). None was tested on a device.

## Summary

- **Korean is live, in beta.** Apple announced on 2026-10-26 (US time; 10-27 KST) that the 27.2 updates (iOS, iPadOS, macOS, watchOS, visionOS) bring Siri AI to Korean, French, Japanese, Portuguese and Spanish, alongside English [1][2][7][8].
- **What's new:** Apple calls Siri AI "an entirely new version of Siri." It understands personal context (messages, mail, photos), knows what is on screen, acts inside apps including some third-party ones, answers broad world-knowledge questions with follow-ups, has a camera "Siri mode" (Visual Intelligence) and writing tools, and keeps a conversation history that syncs through iCloud [1][2][10].
- **How to turn it on (per Apple Support):** update, then go to **Settings > Siri > "Try Siri AI (Beta)"**, choose a voice, complete voice enrollment and review privacy. You then join a **waitlist**, and Siri AI downloads automatically when your turn comes. Device language and Siri language must match a supported language [3]. A Korean blog reports the Korean label as "Siri AI(베타) 체험", but Apple has not confirmed it [18].
- **Requirements:** an Apple Intelligence-capable device (see Apple's list [3][4]), age 13 or older [1][2], an Apple Account in an eligible region (not available on iOS/iPadOS/watchOS in the EU, or with mainland China accounts) [2][3], and up to 8 GB of storage (up to 14 GB on top-tier models) [4].
- **Limits:** server-based features, Siri AI included, have usage limits that vary "by feature, request complexity, system demand." When you hit one, the feature returns "after a time out period." Apple says expanded access "will be available for a fee" in the future, with **no price or date announced** [1][5][11].
- **Privacy and models:** requests run on device or on Apple's **Private Cloud Compute** (비공개 클라우드 컴퓨팅), which Apple says does not store personal data or make it accessible to anyone, Apple included. Apple's Korean release says the new Apple Foundation Model was custom-built "based on a collaboration with Google and Gemini models" [1][13][14].

## 1. Background: Old Siri vs. Siri AI (plain language)

- **Old Siri** handled mostly single commands (timers, calls, weather). It did not dig into your messages, mail or photos, and it could not understand what was on screen. Apple now presents Siri AI as "an entirely new version of Siri" built on Apple Intelligence [2]. Korean coverage lists the differences as stronger personal-context and on-screen understanding, carrying out actions inside apps rather than just answering, camera integration, and continuing a conversation across devices [15].
- **Timeline:**
  - 2026-06-08: Siri AI announced, with developer testing starting [10].
  - 2026-09-14: iOS 27 shipped Siri AI as an **English-only beta**. Korean was promised "next month" [15][16].
  - 2026-10-26 (US): Korean added in 27.2 [1][2].
- **Old Siri is still on the phone.** BGR reports that iOS 27 runs the older Siri by default until you opt in to Siri AI [16]. A search snippet attributed to Apple Support mentions a "Use Siri Classic" option for switching back, but the support page we read does not show it. **Unverified.**

## 2. Current State: How to Turn It On

### 2.1 Update
- Settings > General > Software Update → install iOS 27.2 [17]. This is the standard iOS path. The Korean labels (설정 > 일반 > 소프트웨어 업데이트) come from Korean guides [17][18].

### 2.2 Language settings
- Device language and Siri language must **both** be set to the same supported language, here Korean [1][3][4].
- Korean guide paths: 설정 > 일반 > 언어 및 지역, and 설정 > Siri > 언어 [18]. These are blog-reported and match standard iOS menus, but Apple's Korean UI was not checked first-hand.
- If you have just changed the language, features may stay limited until the new language data finishes installing (blog-reported) [18].

### 2.3 Turn on Siri AI (waitlist)
- Apple Support (English, published 2026-10-22): Settings > **Siri** > **"Try Siri AI (Beta)"**. If Siri is off, turn Siri on first. Then follow the steps to pick a voice, complete voice enrollment and review privacy settings. This "adds you to a waitlist"; wait times vary, and Siri AI downloads automatically when your wait is over [3].
- BGR describes the button sequence as "Try Siri AI (Beta)" → "Join Waitlist" → "Continue". You are offered the option to share audio and text with Apple, which you can decline ("Not Now"). Afterwards the label shows "Joined Waiting List" [16].
- **Korean UI labels (unverified):** a Korean blog gives "Siri AI(베타) 체험" (also "새로운 Siri AI(베타) 체험") [18]. The Korean Apple Support page displays the steps in English only, so the Korean labels cannot be confirmed from Apple [3].
- **Menu-name conflict:** some guides send users to "Apple Intelligence 및 Siri" (Apple Intelligence & Siri) instead of "Siri" [18]. Apple's support page says **Settings > Siri** [3]. For the blog, show the user's own screenshot.
- **No fixed approval time.** Apple says only that wait times vary. A blog mentions unofficial reports of "a few hours to a day" and warns against treating that as guaranteed [3][18].
- Recommended while it downloads: Wi-Fi, a charger and enough free storage (blog advice) [17][18].

### 2.4 Eligibility
- **Devices:** link Apple's pages instead of listing models: "How to get Siri AI" [3] and the Korean "차세대 Apple Intelligence 시작하기" [4]. (For reference only: both Apple pages list iPhone 15 Pro/Pro Max, the iPhone 16 family and later, iPhone Air and iPhone Duo. The standard iPhone 15/15 Plus is not listed [3][4].)
- **Apple Watch discrepancy:** Apple's support pages say Series 9 or later [3][4], while a June report said Series 10 or later [10]. Trust Apple's page.
- **Storage:** up to 8 GB on supported devices, up to 14 GB on devices that meet the higher system requirements, and up to 1.5 GB on Apple Watch. Usage can run higher temporarily during updates [4].
- **Age:** not available to users under 13 [1][2][14].
- **Region:** the Apple Account must be in an eligible region. Siri AI is not available on iOS/iPadOS/watchOS in the EU and does not work with mainland China accounts. Once it is on, it keeps working when you travel [3].
- **Note:** when we read it, Apple's "How to get Siri AI" page (dated 2026-10-22) still said Siri AI is "currently available only in English," which predates the 27.2 announcement [3]. The Newsroom (10-26) is the newer authority on languages [1][2].

### 2.5 Ways to call Siri AI
- iPhone: "Siri야" (Hey Siri), the side button, or swiping down from the Dynamic Island. iPad/Mac: through Spotlight. The Mac also has Control-click menus and a keyboard shortcut for Visual Intelligence [10][13][19].

## 3. Key Features in Korean, with 10+ Example Commands

All features below are listed in Apple's Korean Newsroom release for the Korean launch [1] unless noted. "Documented" means Apple or the press describes the scenario. "Inferred" means our own Korean wording of a documented capability. Behavior in the beta may differ; label the commands as "예시" (examples) in the blog.

| # | Feature | Example command (Korean) | Basis |
|---|---|---|---|
| 1 | Search messages (personal context) | "주말에 엄마가 뭐 하자고 했지?" | **Documented**: Apple KR: asking "what Mom suggested doing during the weekend visit" [1] |
| 2 | Mail → Reminders across apps | "할머니가 메일로 보낸 호박죽 재료, 장보기 목록에 넣어 줘" | **Documented** scenario: pumpkin porridge plan in Messages, recipe from Grandma's email, ingredients into a Reminders shopping list [13][14] |
| 3 | Photo search + follow-up | "작년 제주도에서 찍은 가족사진 찾아 줘" → "그중에 바다 나온 사진만 보여 줘" | Photo search **documented** [1][2]. Wording **reported** by a Korean guide [17] |
| 4 | On-screen → Calendar | (on a friend's wedding website) "이 결혼식 일정, 장소까지 넣어서 캘린더에 추가해 줘" | **Documented** [1][14] |
| 5 | Camera Siri mode (Visual Intelligence) | (pointing the camera at a festival poster) "내가 좋아하는 아티스트 공연 시간 언제야? 캘린더에 넣어 줘" | **Documented** [1][14] |
| 6 | Writing from scratch + revision | "팀장님께 내일 회의를 30분 미뤄 달라는 메일 초안 써 줘" → "조금 더 정중하게 고쳐 줘" | Drafting and spoken revisions **documented** [1][10]. Command **inferred** |
| 7 | Tone-aware writing in Mail/Messages | "친구한테 생일 축하 메시지 써 줘" | Recipient-specific tone and punctuation **documented** [1]. Command **inferred** |
| 8 | Photo edit & share | "방금 찍은 사진 보정해서 엄마한테 보내 줘" | "Editing and sharing photos" **documented** [2][14]. Command **inferred** |
| 9 | Third-party apps | "Todoist에 '보고서 제출' 할 일 추가해 줘" / "WhatsApp으로 친구한테 메시지 보내 줘" | **Documented** apps: WhatsApp, Audible, Craft, Notability, Todoist [1][13][14]. Korean apps (KakaoTalk, Naver, etc.) were **not mentioned**: unverified |
| 10 | World knowledge + follow-ups | "아이들이랑 걷기 좋은 숲길 추천해 줘" → "그 길 얼마나 길어? 아이들이 걷기에 무리 없어?" | **Documented** follow-up example [1] |
| 11 | Calendar attendees (27.2 addition) | "다음 주 회의 참석자가 누구야?" | Calendar attendees as a 27.2 data source **documented** [7]. Wording **reported** [17] |
| 12 | Conversation recall (27.2 addition) | "지난주에 추천해 준 식당 어디였지?" | "Revisit earlier exchanges" **documented** [7]. Korean wording is **inferred** (seen in a search snippet of a Korean guide; page not opened) |
| 13 | Synced history across devices | Start on iPhone, continue in the Siri app on Mac/iPad | **Documented**: history "syncs privately through iCloud" [1][10][15] |
| 14 | Screen content on Mac/iPad | (Mac) Visual Intelligence keyboard shortcut → select an area → ask | **Documented** [1][13] |

Other 27.2 additions: Siri AI can also use photos attached in Messages, voicemails, and Safari history and Reading List. You can select and copy part of a Siri reply. A new "Excluded Apps" setting controls which apps Siri, Search and suggestions can access [7]. **The Korean name and menu location of "Excluded Apps" were not found.**

Not suitable for Korea, though documented elsewhere: splitting a bill with Apple Cash in Camera mode [10]. Apple Cash is a US service, so leave it out.

## 4. Data & Numbers

| Item | Value | Source |
|---|---|---|
| Korean launch | 2026-10-26 US / 10-27 KST, 27.2 updates | [1][2][13][14] |
| Siri AI languages now | 6 (Korean, English, French, Japanese, Portuguese, Spanish) | [1][8] |
| Next languages | Chinese (Traditional), Norwegian, Turkish, Vietnamese, "by the end of the year" | [2][8] |
| English beta launch | 2026-09-14 (iOS 27) | [11][15] |
| Minimum age | 13 | [1][2] |
| Storage | up to 8 GB / up to 14 GB (top tier) / 1.5 GB Watch | [4] |
| Apple Intelligence languages (iOS) | 16, including Korean | [1][4] |
| Usage-limit amount / reset time | **Not published** | [5][11] |
| Paid tier price / date | **Not announced** | [1][5][9] |

## 5. Trends & Outlook

- **More languages soon:** four more languages are due by year-end. 9to5Mac expects them with iOS 27.3 in December, but that is the outlet's speculation [8].
- **Paid tier:** Apple's usage-limit page says "Increased access to such features will be available for a fee." It ties this to the "2027 software releases" [5][11]. At WWDC, Apple said higher **iCloud+** tiers will include expanded access [11][12]. The exact link between iCloud+ and the "fee" is not spelled out.
- **Still beta:** Apple labels Siri AI beta in all 27.2 operating systems [1][2].

## 6. Issues, Limits & Privacy

- **Beta accuracy:** answers can be wrong. A Korean guide advises double-checking dates and amounts against the original message or mail [17].
- **Usage limits:** Apple says limits "may vary by feature, request complexity, system demand, system policies, and other factors." When you reach one, the feature becomes available again "after a time out period." Features covered "include but aren't limited to" Siri AI, intelligent photo editing (Clean Up, Extend, Spatial Reframing), Image Playground, AFM 3 Cloud/Cloud Pro models in Shortcuts, and developer apps using Private Cloud Compute [5]. Apple does not say whether purely on-device features are exempt [5].
- **Terms:** Apple's Apple Intelligence Usage Terms (2026-09-09) let Apple restrict or throttle "excessive, abusive, automated" use and change features at any time [6].
- **Privacy:**
  - Siri AI runs on Apple's next-generation Foundation Models on device and uses servers only when needed [10].
  - Key components (the Spotlight index, App Toolbox) run on device [1][10].
  - With Private Cloud Compute, Apple says personal data "is not stored or made accessible to Apple or anyone else," and independent experts can verify this [1][10].
  - BGR notes the setup offers optional sharing of audio and text with Apple, which you can decline [16].
- **Gemini wording:** Apple's Korean release says the new Apple Foundation Model was "custom-developed based on a collaboration with Google and Gemini models" [1][14]. Do not say "Siri is Gemini." Use "according to Apple's announcement."
- **Third-party coverage:** Apple names WhatsApp, Audible, Craft, Notability and Todoist. Support for Korean apps is not documented.
- **Screen Time / managed devices:** check Settings > Screen Time for restrictions. Do not remove an MDM profile on a work phone (blog advice) [18].

## 7. FAQ Material (common searches)

1. **"시리 AI 한국어 언제부터?"** (Since when is it in Korean?) → Since iOS 27.2, released 2026-10-26 US / 10-27 KST [1][13].
2. **"내 아이폰도 되나요?"** (Does my iPhone work?) → It needs an Apple Intelligence-capable device. Check Apple's list [3][4]. The standard iPhone 15/15 Plus is not on Apple's list [3][4].
3. **"업데이트했는데 시리가 그대로예요"** (I updated but Siri is the same) → You have to opt in through Settings > Siri > "Try Siri AI (Beta)" and wait for the waitlist. Until then the old Siri is active [3][16].
4. **"대기 시간 얼마나 걸려요?"** (How long is the wait?) → Apple gives no fixed time [3]. Do not reset your phone to speed it up [18].
5. **"메뉴가 안 보여요"** (I can't find the menu) → Check the device, that device and Siri language match, the account region, age 13+, Screen Time restrictions, and storage [3][4][18].
6. **"무료예요?"** (Is it free?) → Yes for now, within daily limits. A paid option for more use is planned; the price is not announced [1][5].
7. **"한도 넘으면?"** (What if I hit the limit?) → That feature pauses until a time-out period ends. Other features keep working [5][6].
8. **"개인정보 괜찮아요?"** (Is my privacy safe?) → It works on device plus Private Cloud Compute, and Apple says data is not stored [1][10].
9. **"제미나이가 들어간 거예요?"** (Does it use Gemini?) → Apple says its new model was built "based on a collaboration with Google and Gemini models" [1].
10. **"아이 폰에서도 되나요?"** (Can my child use it?) → No, not for users under 13 [1].
11. **"카카오톡도 되나요?"** (Does it work with KakaoTalk?) → Not documented. Apple names WhatsApp, Todoist and others [1]. Test before claiming.
12. **"해외 가서도 돼요?"** (Does it work abroad?) → Yes, once it is on, according to Apple. The EU and mainland China account restrictions apply [3].

## 8. Unverified / Flagged Points

- Korean UI labels ("Siri AI(베타) 체험", "Apple Intelligence 및 Siri") come from blogs only, and guides disagree on whether the path goes through "Siri" or "Apple Intelligence 및 Siri." **Confirm with an on-device screenshot.**
- The "Use Siri Classic" switch-back option was not confirmed on a page we read.
- Apple's "How to get Siri AI" page still said "English only" when read (published 10-22, before the Korean launch).
- Apple Watch: Series 9 (Apple Support) vs Series 10 (June report).
- No numeric usage cap, reset time or paid price exists in any source.
- How well Korean speech recognition works and how accurate it is: no substantive hands-on review was found.
- Example commands marked "inferred" or "reported" have not been tested on a device.
- Support for Korean third-party apps is undocumented.
- The Korean name of the "Excluded Apps" setting was not found.
- The Apple Newsroom pages were read through a summarizing fetch tool; short quotes are as returned, so check the exact wording on the pages before quoting at length.

## Sources

1. [Siri AI, 오늘부터 더 많은 언어로 이용 가능](https://www.apple.com/kr/newsroom/2026/10/siri-ai-is-available-today-in-more-languages/) — Apple Newsroom (Korea), 2026-10-26
2. [Siri AI is available in more languages starting today](https://www.apple.com/newsroom/2026/10/siri-ai-is-available-in-more-languages-starting-today/) — Apple Newsroom, 2026-10-26
3. [How to get Siri AI](https://support.apple.com/en-us/127893) (Korean locale: https://support.apple.com/ko-kr/127893) — Apple Support, published 2026-10-22
4. [차세대 Apple Intelligence 시작하기](https://support.apple.com/ko-kr/121115) — Apple Support (Korea), 2026-10-23
5. [Learn about Apple Intelligence usage limits](https://support.apple.com/en-us/127901) (Korean: https://support.apple.com/ko-kr/127901) — Apple Support, 2026-09-09
6. [Apple Intelligence Usage Terms](https://support.apple.com/en-us/148587) — Apple Support, 2026-09-09
7. [Apple Releases iOS 27.2 With New Siri AI Languages](https://www.macrumors.com/2026/10/26/apple-releases-ios-27-2/) — MacRumors, 2026-10-26
8. [Apple announces Siri AI will expand to these new languages soon](https://9to5mac.com/2026/10/26/apple-announces-siri-ai-will-expand-to-these-new-languages-soon/) — 9to5Mac, 2026-10-26
9. [Siri AI Gets Five New Languages and Apple Says You'll Have to Pay for Expanded Access](https://gadgets.beebom.com/news/siri-ai-gets-five-new-languages-with-ios-27-2-update) — Beebom, updated 2026-10-28
10. [Apple Introduces Siri AI With Personal Context and Onscreen Awareness](https://www.iclarified.com/101113/apple-introduces-siri-ai-with-personal-context-and-onscreen-awareness) — iClarified, 2026-06-08
11. [Apple's Fine Print: Daily Usage Limits for Siri AI, 'Expanded Access' Coming for a Fee](https://macrumors.com/2026/09/09/apple-siri-ai-usage-limits/) — MacRumors, 2026-09-09
12. [New AI Siri Compatible Devices: Supported iPhone, iPad and Mac List](https://www.iphoneincanada.ca/2026/06/08/new-ai-siri-compatible-devices-supported-iphone-ipad-and-mac-list/) — iPhone in Canada, 2026-06-08
13. [Siri AI Korean-language launch report](https://www.fnnews.com/news/202610270926188986) — Financial News (파이낸셜뉴스), 2026-10-27
14. [아이폰 쓰는 사람들 주목…애플이 드디어 한국어로 선보인 '이 기능' 정체](https://www.wikitree.co.kr/articles/1169430) — Wikitree, 2026-10-27
15. [애플 '시리 AI' 마침내 출격⋯10월 한국어 지원](https://www.inews24.com/view/2005992) — iNews24, 2026-09-15
16. [How To Get Siri AI After Updating To iOS 27](https://www.bgr.com/2265148/how-to-enable-siri-ai-ios-27-guide/) — BGR, 2026-09-22
17. [시리 AI 한국어 사용법, 켜는 순서와 사진 찾기 예시](https://www.digitalmarketer.co.kr/insights/siri-ai-korean-ios-27-2) — Digital Marketer (blog/guide), 2026-10 (exact date not shown)
18. [iOS 27.2 시리 AI 한국어 대기자 명단 신청·승인·활성화 오류 해결](https://yellowit.co.kr/it-review/ios-27-2-%EC%8B%9C%EB%A6%AC-ai-%ED%95%9C%EA%B5%AD%EC%96%B4-%EB%8C%80%EA%B8%B0%EC%9E%90-%EB%AA%85%EB%8B%A8-%EC%8B%A0%EC%B2%AD%C2%B7%EC%8A%B9%EC%9D%B8%C2%B7%ED%99%9C%EC%84%B1%ED%99%94-%EC%98%A4%EB%A5%98/) — 노랗IT월드 (blog), 2026-10-29
19. [Siri AI, 오늘부터 한국어로 이용 가능 (27.2 소프트웨어 업데이트)](https://www.clien.net/service/board/news/19283153) — Clien (community repost of Apple KR Newsroom), 2026-10-27
