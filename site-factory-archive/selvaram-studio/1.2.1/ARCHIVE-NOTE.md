# Selvaram Studio archive note

The user explicitly approved preserving the previous accepted Selvaram Studio theme before the next batch BUILD.

Accepted artifact:
- theme: `selvaram-studio-v1.2.1.zip`
- theme root: `selvaram-studio/`
- version: `1.2.1`
- product: `Underground Racing`
- GEO / locale: `PL / pl-PL`
- SHA-256: `696c3aa57fe188edd1b8e8313ff414b9bc488b83cc02f3e786cc099236a64950`
- ZIP entries: `97`

Archive-key note:
- the accepted artifact does not embed a production DOMAIN, so this Git path uses the immutable theme/site key `selvaram-studio` instead of inventing a domain.

Binary-archive limitation:
- the exact ZIP remains the authoritative delivered artifact in the user's Library;
- the current GitHub connector does not accept a local container file reference for binary upload;
- therefore Git stores the verified manifest, QA, SHA-256 identity and this archive note;
- this must not be described as a complete binary Git theme archive until `theme.zip` is actually committed.
