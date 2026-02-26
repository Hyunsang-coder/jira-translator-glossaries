# jira-translator-glossaries

[jira-translator](https://github.com/Hyunsang-coder/jira-translator) Lambda 함수에서 사용하는 게임 용어집 파일 모음입니다.

glossary 파일만 수정하고 push하면 Lambda 재배포 없이 즉시 반영됩니다.

## 파일 구성

| 파일 | 프로젝트 | 이슈 키 |
|------|----------|---------|
| `pbb_glossary.json` | PBB (Project Black Budget) | `P2-` |
| `heist_glossary.json` | Heist Royale | `PAYDAY-` |
| `pubg_glossary.json` | PUBG | `PUBG-` |
| `bsg_glossary.json` | BSG | `PUBGXBSG-` |

## 포맷

```json
{
  "project": "프로젝트명",
  "glossary": {
    "카테고리": [
      { "ko": "한국어", "en": "English" },
      { "ko": "저격수", "en": "Sniper", "note": "적 enemy 타입. 플레이어 클래스는 Marksman" }
    ]
  }
}
```

- `ko`, `en` 필수 / `note` 선택 (LLM이 동음이의어 구분에 활용)
- 카테고리명은 자유롭게 추가 가능
