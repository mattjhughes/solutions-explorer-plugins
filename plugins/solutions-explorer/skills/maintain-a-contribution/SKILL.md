---
name: maintain-a-contribution
description: Guide updates, revision review, private feedback review, unpublishing, republishing, and edit-token replacement for a CSU Solutions Explorer contribution through its owner-management UI. Use when a user wants to maintain an existing contribution.
---

Use the connected Solutions Explorer MCP app and its discovered tool namespace. A contributor's name, campus, chat identity, or matching title does not authorize owner actions. The server verifies the contribution's edit token inside the widget.

If the user supplied a contribution ID, open `render_explorer` with `view: "manage"` and that `entry_id`. Otherwise, search published entries by the supplied title with `search_solutions` and let the user identify the right result. For an unpublished entry or one absent from search, open management so the user can enter its ID from their receipt. Do not conclude that an absent public result was deleted.

Ask the user to enter the edit token only in the widget. Never solicit, echo, place in a draft, or transmit it through a model-facing tool. If they paste a token into chat, do not repeat it; direct them to the widget's token-replacement control. Do not claim that the conversation copy has been removed.

Help draft requested wording changes in the conversation using public material or details the user chooses to share. Pass only proposed changed fields as `draft` with `render_explorer`, `view: "manage"`, and the selected `entry_id`. After private token entry, the UI merges those fields with the current solution and shows current/proposed wording before saving. Never include a token or private feedback in the draft. Keep unrelated fields out of the proposed changes. The management UI handles unlock, private feedback, revisions, complete edits, added attachments, publication status, and token replacement. Do not call widget-only owner tools from the conversation or claim access to private metadata. Feedback stays in the owner inbox unless the user chooses to share an excerpt.

The current widget supports adding attachments, not deleting or replacing existing ones. Token replacement invalidates the old token and displays the new one once. Unpublishing removes an entry from public discovery; it is not deletion. Explain these consequences when relevant to the requested action.

On a stale-version error, guide the user to reload the latest entry, compare revisions, and reapply their intended change. Do not overwrite a newer revision or blindly retry a write. After an interrupted token replacement or publication, do not promise token recovery; this demo has no account recovery or server copy of the secret.

Opening management or drafting text does not save an edit. Report a change as completed only when its tool result confirms it or the user reports successful completion; attribute user-reported status accordingly. If the app or tunnel is unavailable, identify the connection problem and preserve the requested draft without implying it was persisted.
