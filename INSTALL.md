# INSTALL — 이 키트를 작업 폴더에 설치하는 방법 (Codex가 읽고 실행)

> 사용자가 "INSTALL.md대로 설치해줘"라고 하면 아래를 **순서대로 전부, 중간에 묻지 않고** 실행한다. 끝나면 결과를 `ls -a`로 보여준다.
>
> **미리 허락된 것 (다시 묻지 않는다):** 같은 이름 파일은 덮어쓴다 · 백업은 필요 없다 · 키트 폴더는 삭제한다 · `/quit`은 사용자가 직접 한다. 과제 README.md만 건드리지 않는다.

## 전제
- 이 파일은 `git clone`으로 받은 키트 폴더(예: `kit/` 또는 `hackathon-kit/`) 안에 있다.
- **작업 폴더** = 과제 README.md가 있는 곳 (보통 `/home/user`, 현재 폴더). 키트 폴더의 한 단계 위.

## 할 일 (키트 폴더 이름을 `KIT`이라고 할 때)

1. 아래를 **작업 폴더 최상위로 복사**한다. 이미 같은 이름이 있으면 덮어쓴다. 키트에 없는 항목은 건너뛴다.
   - `KIT/AGENTS.md`
   - `KIT/cheatsheet.md`
   - `KIT/docs/` (폴더째)
   - `KIT/.agents/` (폴더째 — 숨김 폴더)
   - `KIT/scripts/` (폴더째)
2. `KIT/starter/web/`이 있으면 **안의 내용물**(`server.js`, `public/`)을 작업 폴더 최상위로 복사한다. 없으면 건너뛴다.
3. **복사하지 않는 것**: `KIT/README.md`, `KIT/INSTALL.md`, `KIT/.git/`, `KIT/starter/` 폴더 자체. 과제의 README.md는 절대 건드리지 않는다.
4. 키트 폴더 `KIT/`를 통째로 삭제한다.
5. `ls -a`를 실행해 결과를 보여준다.
6. 사용자에게 한 줄로 알린다: **"설치 끝. AGENTS.md를 인식시키려면 `/quit` 후 `codex`를 다시 켜세요."**

## Codex도 못 할 때 (수동 대체)
사용자가 터미널에서 직접: 최소한 `AGENTS.md`와 `docs/` 폴더만 최상위에 복사하면 규칙은 동작한다.
```bash
cp KIT/AGENTS.md . && cp -r KIT/docs . && rm -rf KIT
```
