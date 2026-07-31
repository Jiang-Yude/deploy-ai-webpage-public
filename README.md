# deploy-ai-webpage-public

把 AI 做好的網頁，變成一個朋友點開就能看的網址。

這是一個**公開、給新手用的 AI 技能包（skill）**。它教 AI 一步一步帶你，把你用 AI 做出來的網頁（HTML / CSS / JavaScript）放到網路上，拿到一個可以分享的連結——用 GitHub Pages 或 Vercel，並在發佈前幫你檢查內容適不適合公開。

你不用懂程式。看不懂的部分，照著把指令丟給 AI，它會幫你做完。

---

## 怎麼安裝（給 Codex / Claude 等 AI 代理）

把這個 repo 的網址丟給你的 AI 代理（例如 Codex），請它幫你安裝這個技能包即可：

```
請幫我安裝這個技能包：https://github.com/Jiang-Yude/deploy-ai-webpage-public
```

> 前提：你要先設定好你的 AI 代理跟 GitHub 的連線（登入 / 授權）。連線設定好之後，給網址、它就能抓下來安裝。

安裝後，直接對 AI 說：

```
請幫我部署這個 AI 做好的網頁。先檢查是否適合公開，再推薦 GitHub Pages 或 Vercel，完成後給我可以分享的網址。
```

---

## 這個技能包會幫你做什麼

1. 先檢查網頁能不能公開（有沒有夾帶私人資料）。
2. 判斷該用 GitHub Pages 還是 Vercel。
3. 一步一步引導你完成部署。
4. 驗證最後的網址能不能正常打開。
5. 把你自己的踩坑與常用指令，記錄回技能包的個人筆記區，越用越順手。

## 內容

- `SKILL.md` — 技能包主檔
- `references/01-decision-and-safety.md` — 該用哪個平台、公開安全檢查
- `references/02-github-pages.md` — GitHub Pages 部署
- `references/03-vercel.md` — Vercel 部署
- `references/04-personal-notes-template.md` — 你的個人筆記範本
- `agents/openai.yaml` — 代理設定

## 授權

MIT

---

## 維護者

江昱德（Jiang Yude）<br>
隱性知識提煉師<br>
AI 知識架構師

[知識官網](https://jiangyude.com/) · [Threads](https://www.threads.com/@jiang_yude_coach)
