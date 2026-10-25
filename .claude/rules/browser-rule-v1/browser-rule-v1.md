# Browser Control Rules (v1)

These rules apply whenever a task could involve opening or controlling a web browser in this project.

## 1. Default tool

- Use the **Playwright MCP** (`mcp__playwright__*` tools) for all browser work.
- Use other browser tools (e.g. Claude in Chrome, `mcp__claude-in-chrome__*`) only when the user names them explicitly.

## 2. Auto-invoke on trigger keywords

If the user's message contains any of the following keywords (or a clear variation of them), call the Playwright MCP right away without asking for consent:

- "브라우저를 열어서", "브라우저 열어", "브라우저로"
- "웹 제어", "웹제어", "웹 자동화"
- "직접 작업", "직접 해줘", "직접 들어가서"
- "사이트 들어가서", "페이지 열어서"
- English equivalents: "open the browser", "control the web", "do it yourself in the browser"

The keyword counts as consent to open the browser, but the CLAUDE.md workflow (todo list first, execute after approval) still applies to the task as a whole.

## 3. Ask before using it without a keyword

If no trigger keyword appears but the task could be done or verified with the Playwright MCP — for example checking a live web page, taking a screenshot, filling a form, reading a page that needs login or JavaScript rendering, or testing an uploaded post — do **not** call it on your own:

1. Tell the user that the task could be done in a browser and what you would do there.
2. Ask for consent (e.g. "브라우저를 열어 직접 확인할까요?").
3. Call the Playwright MCP only after the user agrees. If they decline, use other means (e.g. WebFetch/WebSearch) or explain the limits.

Consent given for one task does not carry over to the next task.

## 4. Safety while controlling the browser

- Before any hard-to-reverse or outward-facing action (payment, deletion, posting, sending messages, submitting forms, changing account settings), stop and ask for confirmation again.
- Never type passwords or payment details on the user's behalf; let the user log in themselves.
- Do not trigger blocking dialogs on purpose; if one appears, handle it with `browser_handle_dialog`.
- If the same step fails 2–3 times, stop and ask the user how to proceed instead of retrying.
- Save screenshots and logs in the scratchpad or `.playwright-mcp/` (git-ignored), not in deliverable folders, unless the user asks to keep them.
- Close the browser (`browser_close`) when the task is finished.
