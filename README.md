# jira-translator-glossaries

[jira-translator](https://github.com/Hyunsang-coder/jira-translator) Lambda 함수에서 사용하는 게임 용어집 파일 모음입니다.

glossary 파일만 수정하고 push하면 Lambda 재배포 없이 즉시 반영됩니다.

## 네이밍 규칙

- **독립 게임 프로젝트**: `{게임}_glossary.json`
- **게임 내 모드**: `{게임}_{모드}_glossary.json`

## 파일 구성

| 파일 | 프로젝트 | 비고 |
|------|----------|------|
| `pubg_glossary.json` | PUBG | 코어 용어 (공식 패치노트 기반) |
| `pubg_heist_glossary.json` | PUBG Heist Royale | Heist Royale 모드 전용 |
| `pubg_binaryspot_glossary.json` | PUBG BinarySpot | BinarySpot 모드 전용 |
| `pubg_outbreak_glossary.json` | PUBG Outbreak | Outbreak 모드 전용 |
| `pbb_glossary.json` | PBB (Project Black Budget) | |

### 번역 시 glossary 로드 방식

- PUBG 코어 티켓: `pubg_glossary.json`
- PUBG 모드 티켓: `pubg_glossary.json` + 해당 모드 파일

## 포맷

```json
{
  "project": "PUBG Heist Royale",
  "glossary": {
    "카테고리": [
      { "ko": "한국어", "en": "English" },
      { "ko": "저격수", "en": "Sniper", "note": "적 enemy 타입. 플레이어 클래스는 Marksman" }
    ]
  }
}
```

- `ko`, `en` 필수 / `note` 선택 (LLM이 동음이의어 구분에 활용)
- `project` 값: 독립 게임은 게임명, 모드는 `"{게임} {모드명}"` 형식
- 카테고리명은 자유롭게 추가 가능
