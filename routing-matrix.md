# story-room routing matrix

This file maps problem types to owner, patch depth, upstream checks, and downstream impact.

---

## 1. Hook-related issues

| Problem | Default Owner | Patch Depth | Patch Hook Board First | Downstream Stale Risk |
|---|---|---:|---|---|
| Opening hook weak | plot-agent / script-agent | 1-3 | often yes | script, storyboard |
| Audience question unclear | plot-agent | 2-3 | yes | script, storyboard |
| First reversal too late | plot-agent / script-agent | 2-3 | usually yes | script, storyboard |
| Cliffhanger weak | plot-agent / script-agent | 1-3 | often yes | storyboard |

---

## 2. Character-related issues

| Problem | Default Owner | Patch Depth | Patch Hook Board First | Downstream Stale Risk |
|---|---|---:|---|---|
| Motivation unclear | character-agent | 1-2 | no, unless spine changes | script, storyboard |
| Relationship tension weak | character-agent | 1-2 | no | script |
| Emotional pivot unsupported | character-agent / script-agent | 1-2 | sometimes | script, storyboard |
| Voice separation weak | character-agent / script-agent | 1-2 | no | script |

---

## 3. Script execution issues

| Problem | Default Owner | Patch Depth | Patch Hook Board First | Downstream Stale Risk |
|---|---|---:|---|---|
| Scene drag | script-agent | 1-2 | no | storyboard |
| Conflict escalation weak | script-agent | 1-2 | no | storyboard |
| Dialogue too expository | script-agent | 1-2 | no | storyboard |
| Exit hook weak | script-agent | 1-2 | no, unless ending spine changes | storyboard |
| Payoff soft | script-agent / plot-agent | 1-3 | sometimes | storyboard |

---

## 4. Storyboard issues

| Problem | Default Owner | Patch Depth | Patch Hook Board First | Downstream Stale Risk |
|---|---|---:|---|---|
| Coverage unclear | storyboard-agent | 1-2 | no | low |
| Visual emphasis weak | storyboard-agent | 1-2 | no | low |
| Reversal image weak | storyboard-agent / script-agent | 1-2 | no, unless story beat changes | low-medium |
| Cliffhanger shot weak | storyboard-agent / script-agent | 1-2 | no, unless cliffhanger changes | low-medium |
| Production plan clumsy | storyboard-agent | 1-2 | no | low |

---

## 5. Restart triggers

| Condition | Default Action |
|---|---|
| Premise collapse | structural patch or restart |
| Hook spine contradiction | patch hook board before anything downstream |
| Multiple layers broken because of one upstream flaw | patch upstream owner first |
| Repeated failure after two passes | escalate patch depth or stop |

---

## 6. Practical ordering rule

When several issues appear at once, use this order:
1. fix hook spine
2. fix motivation support
3. fix scene execution
4. fix visual translation

This protects system continuity and reduces wasteful rework.
