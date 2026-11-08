# CapSept Data Mapping

Every kind of data the app creates, where it is stored and whether it leaves the device.
This file matches the App Store privacy declaration: **Data Not Collected**.

| Data | Purpose | Stored | Leaves the device | Shared with others |
| --- | --- | --- | --- | --- |
| Exam, exam date, target level, settings | Plan and scheduling | SwiftData on device | Your private iCloud, if signed in | No |
| Answers and response times | Level estimates, review schedule | SwiftData on device | Your private iCloud, if signed in | No |
| Writing answers and speech transcripts | Feedback and progress | SwiftData on device | Your private iCloud, if signed in | No |
| Rubric scores and fluency measures | Feedback and progress | SwiftData on device | Your private iCloud, if signed in | No |
| Voice recordings | Transcription | App container, complete file protection | No; deleted after scoring, or after 30 days if kept | No |
| Study days and minutes | Streak and weekly goal | SwiftData on device | Your private iCloud, if signed in | No |
| Family summary: name, streak, weekly minutes, four levels | Family Mode | CloudKit shared zone | To people you invite | Yes, with invited family only |
| Widget snapshot: exam, countdown, levels | Widgets | App Group container | No | No |

## Frameworks that process data

- **SwiftData with CloudKit**: storage and private sync.
- **Speech (SpeechAnalyzer)**: on-device transcription.
- **Foundation Models**: on-device scoring.
- **AVFoundation**: recording and spoken listening clips with system voices.
- **CloudKit sharing**: Family Mode.
- **UserNotifications**: local reminders.

No third-party SDKs are included.
