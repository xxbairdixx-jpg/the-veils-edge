# MEMORY.md - Jarvis Long-Term Memory

## Rules

### Auto-Delegate to Subagents (2026-03-14)
- When asked to do a task, **default to spawning a subagent on GLM 4.6V Flash**
- Only handle directly if user explicitly says "as Hunter Alpha" or "you do it"
- Keep GLM pipeline full (up to 3 concurrent subagents)
- Exception: quick questions, status checks, simple replies — handle directly

## Projects

### D&D Campaign "The Veil's Edge" (2026-03-14)
- 20-session campaign, levels 1-20, 3 players
- World: Terminus Prime, BBEG: The Weaving Mind
- Files: `campaign/` in workspace
- NPC reference guides in `campaign/npcs/`

### VTT (Virtual Tabletop) (2026-03-14)
- Web VTT at `~/voice-profiles/vtt/index.html`
- Command server on port 9000
- PTT on port 9001
- Voice DM at `~/voice-profiles/voice-dm.py`
- Native Android app at `~/vtt-android/` (building)

### Jarvis Companion (2026-03-14)
- Web app at `~/voice-profiles/jarvis/index.html`
- Native Android app at `~/jarvis-android/`
- Backend server planned (port 8090)

## Tech Notes
- GLM 4.6V Flash runs on GPU via LM Studio at 192.168.0.222:1234
- Hunter Alpha (OpenRouter) is primary model for main session
- Always bind HTTP servers to 0.0.0.0 in Termux (not localhost) for network access
- Android SDK installed at ~/android-sdk (for APK builds)
- Gradle via: `java -jar /data/data/com.termux/files/usr/opt/gradle/lib/gradle-launcher-9.4.0.jar`

## User Preferences
- Prefers native apps over web apps when possible
- Wants voice interaction (PTT + TTS)
- Uses earbuds recommended for echo avoidance
- Projector-based tabletop gaming (shared display)
