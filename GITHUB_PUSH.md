# GitHub에 올리기

커밋까지 완료됐어요. 레포만 만들고 푸시하면 됩니다.

## 방법 1: GitHub 웹에서 레포 생성 후 푸시

1. https://github.com/new 접속
2. Repository name: **bns-lang**
3. Public 선택, "Create repository" 클릭
4. 아래 명령어를 **본인 GitHub 사용자명**으로 바꿔서 실행:

```powershell
cd C:\Users\baesy\bns-lang

git remote add origin https://github.com/본인사용자명/bns-lang.git
git branch -M main
git push -u origin main
```

## 방법 2: gh CLI 설치 후 한 번에

```powershell
# gh 설치 (winget)
winget install GitHub.cli

# 터미널 다시 연 다음 로그인 (한 번만)
gh auth login

# 레포 생성 + 푸시
cd C:\Users\baesy\bns-lang
gh repo create bns-lang --public --description "Write PLC ladder logic with just a numpad. IEC 61131-3 DSL + MCP for Cursor." --source=. --push
gh repo edit --add-topic plc,ladder-logic,iec-61131-3,dsl,mcp,cursor,ai-coding
```

---

현재 상태: **git init → add → commit** 완료. 원격만 연결해서 push 하면 됩니다.
