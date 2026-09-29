# CablerOS Developer Access & Source Security Policy — DRAFT

**Status:** Draft for legal/security review  
**Draft date:** September 29, 2026

This policy defines the intended security model for private CablerOS source code and developer access. It supplements the CablerOS License.

## 1. Source Location

The authoritative CablerOS source is intended to reside only on CablerOS-controlled infrastructure.

Until dedicated server infrastructure exists, the Head Founder may maintain the authoritative development copy on an approved local system.

Once the CablerOS development server is operational, ordinary development source must remain on CablerOS-controlled systems rather than personal developer computers.

## 2. Individual Approval

Every developer must have an individually approved account.

Organizations or teams may nominate developers, but CablerOS must approve each person before access is granted.

Accounts, passwords, API tokens, SSH keys, session credentials, and other access methods may not be shared.

## 3. Remote Access

Remote access is not automatically granted.

Remote access may be allowed only when:

- CablerOS specifically approves it;
- the developer uses the approved access method;
- required security controls are enabled; and
- access can be centrally revoked and audited.

CablerOS may require MFA, device approval, logging, session controls, or other safeguards.

## 4. No Personal Copies

Developers may not clone, export, copy, archive, or back up private CablerOS source onto personal systems unless specifically authorized in writing.

Screenshots, copied source snippets, personal notes containing private source, and exports to unapproved systems are prohibited.

When access ends, local or exported copies must be deleted unless CablerOS gives written permission to retain a specific archival copy.

## 5. Approved Development Tools

Private source may be processed only by tools and services approved by CablerOS.

External AI assistants, code-analysis services, cloud development tools, or other third-party systems may access private source only when CablerOS has approved both the tool and the intended use and the source remains within approved infrastructure or an expressly approved processing arrangement.

## 6. Immediate Revocation

CablerOS may immediately revoke source access for:

- credential or account sharing;
- unauthorized source disclosure;
- deliberate source leakage;
- circumvention of access controls;
- misuse of approved infrastructure;
- activity creating a material security risk; or
- loss of a current need for access.

Ordinary non-security license violations remain subject to the CablerOS License's normal notice-and-cure process unless immediate access restriction is independently justified for security.

## 7. Team Changes

If a developer leaves an approved organization or team, or no longer needs access, access should be revoked as soon as CablerOS is notified.

## 8. Accidental Exposure

Accidental disclosure must be reported promptly.

CablerOS may immediately suspend source access to contain the incident. Prompt disclosure, cooperation, and remediation should be considered when determining further consequences.

## 9. Authorized Distribution

This policy does not prohibit a distribution expressly authorized by the CablerOS License.

An approved developer may not treat a public release, source disclosure, or fork distribution as authorized unless all applicable CablerOS License requirements are satisfied.

---

**DRAFT — NOT ATTORNEY OR SECURITY-TEAM REVIEWED**
