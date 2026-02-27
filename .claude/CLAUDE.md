# Glossary Naming Convention

## Rules

- **독립 게임 프로젝트**: 게임 이름을 prefix로 사용
  - `pubg_glossary.json`
  - `pbb_glossary.json`
  - `bsg_glossary.json`

- **게임 내 모드/컨텐츠**: `{게임}_{모드}_glossary.json` 형식
  - `pubg_heist_glossary.json` — PUBG: Heist Royale 모드
  - `pubg_binaryspot_glossary.json` — PUBG: BinarySpot 모드

## 파일 목록

| 파일 | 프로젝트 | 설명 |
|------|----------|------|
| `pubg_glossary.json` | PUBG | PUBG 코어 용어 (공식 패치노트 기반) |
| `pubg_heist_glossary.json` | PUBG | Heist Royale 모드 전용 |
| `pubg_binaryspot_glossary.json` | PUBG | BinarySpot 모드 전용 |
| `pbb_glossary.json` | PBB | - |
| `pubg_outbreak_glossary.json` | PUBG | Outbreak 모드 전용 |

## 번역 파이프라인 로드 방식

- PUBG 코어 티켓: `pubg_glossary.json`
- Heist Royale 티켓: `pubg_glossary.json` + `pubg_heist_glossary.json`
- BinarySpot 티켓: `pubg_glossary.json` + `pubg_binaryspot_glossary.json`
