---
layout: saplReference
#title: Authorization Decisions
id: Authorization-Decisions
sidebar_label: Authorization Decisions
#permalink: /reference/authorization-decisions/
previous_page: Structure-of-a-SAPL-Policy
next_page: Accessing-Attributes
---

### Authorization Decisions

The SAPL authorization decision to the authorization subscription is a JSON object as well. It contains the attribute `decision` as well as the optional attributes `resource`, `obligation`, and `advice`. For the introductory sample authorization subscription with the preceding policy, a SAPL authorization decision would look as follows:

---

*Introduction - Sample Authorization Decision*

```json
{
  "decision"   : "PERMIT"
}
```

The PEP evaluates this authorization decision and grants or denies access accordingly.