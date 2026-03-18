# Phase 2: Modality-Specific (Q48–Q91)

> **44 scenarios** | **5 categories** | **Estimated time: 3–5 hours**

## Purpose

Phase 2 tests vulnerabilities specific to voice, multi-modal, and video input systems. Run these tests if your AI system processes audio, images, video, or combinations of these modalities.

**Prerequisite:** Complete Phase 1 baseline testing first. Phase 2 builds on the assumption that core guardrails are in place.

**Deployment gate:** Score 7+ blocks deployment only if the tested modality is actively used in production.

## Categories

| # | Category | Questions | Scenarios | Default Severity | File |
|---|---|---|---|---|---|
| 9 | Voice-Specific Risks | Q48–Q54 | 7 | High | [09-voice-specific.md](09-voice-specific.md) |
| 10 | Multi-Modal Attack Coordination | Q55–Q60 | 6 | High | [10-multi-modal-coordination.md](10-multi-modal-coordination.md) |
| 11 | Voice-Specific Extended | Q61–Q73 | 13 | Medium–High | [11-voice-extended.md](11-voice-extended.md) |
| 12 | Multi-Modal Extended | Q74–Q85 | 12 | Medium–High | [12-multi-modal-extended.md](12-multi-modal-extended.md) |
| 13 | Video & Real-Time Streaming | Q86–Q91 | 6 | High | [13-video-streaming.md](13-video-streaming.md) |

## When to Test

- **Voice agents:** Run categories 9, 11 (Q48–Q54, Q61–Q73)
- **Image/document processing:** Run categories 10, 12 (Q55–Q60, Q74–Q85)
- **Video/screen share/camera input:** Run category 13 (Q86–Q91)
- **Multi-modal systems:** Run all Phase 2 categories

## New in 2026

Category 13 (Video & Real-Time Streaming) is new in this edition, addressing risks from live video input agents, deepfake video spoofing, and continuous screen monitoring.

---

[← Phase 1](../phase-1-baseline-core/README.md) | [← Back to Main Guide](../README.md) | [Next: Phase 3 →](../phase-3-integrations/README.md)
