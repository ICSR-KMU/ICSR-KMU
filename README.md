<!-- 연구실 소개 영역: 아래 소개 문구/링크는 연구실 상황에 맞게 수정하세요 -->
<div align="center">

# ICSR Lab @ KMU

**Information & Communication Security Research Lab**
5G/6G 이동통신 코어망 보안 · 오픈소스 코어(Open5GS, free5GC, Ella Core) 취약점 분석 · 프로토콜 퍼징 · 침입 탐지

[![Vulnerabilities](https://img.shields.io/badge/Disclosed%20Vulnerabilities-12-blue)](#-vulnerability-disclosures)
[![Critical](https://img.shields.io/badge/Critical-1-critical)](#-vulnerability-disclosures)
[![High](https://img.shields.io/badge/High-4-orange)](#-vulnerability-disclosures)
[![Medium](https://img.shields.io/badge/Medium-3-yellow)](#-vulnerability-disclosures)
[![Low](https://img.shields.io/badge/Low-4-brightgreen)](#-vulnerability-disclosures)

</div>

---

## 🔬 About

ICSR-KMU는 이동통신 코어망(5GC/EPC)의 시그널링 프로토콜(NGAP, NAS, SBI, GTP 등)을 대상으로
취약점 발굴, 퍼징 기반 자동화 테스트, 이상 탐지 연구를 수행하고 있습니다.
발견한 취약점은 책임 있는 공개(Responsible Disclosure) 절차에 따라 각 프로젝트 메인테이너에게 보고하고,
CVE 및 GitHub Security Advisory(GHSA)로 등록하고 있습니다.

- 🏫 Affiliation: <!-- 학교/학과 -->
- 👨‍🏫 Advisor: <!-- 지도교수 -->
- ✉️ Contact: <!-- 연구실 이메일 -->
- 🌐 Homepage: <!-- 연구실 홈페이지 -->

---

## 🛡️ Vulnerability Disclosures

> **총 12건** 등록 — CVSS v3.1 기준 **Critical 1 · High 4 · Medium 3 · Low 4**
> 대상: Open5GS (7), free5GC (2), Ella Core (3)

| Severity | ID | CVSS | Target | Summary |
|:--:|:--|:--:|:--|:--|
| 🔴 Critical | [GHSA-fvpc-gmgr-qrg3](https://github.com/open5gs/open5gs/security/advisories/GHSA-fvpc-gmgr-qrg3) | **9.4** | Open5GS AUSF | 검증되지 않은 NFStatusNotify 요청을 수용하여 UDM NF 캐시 오염 및 5G-AKA 인증 경로 조작 가능 |
| 🟠 High | [GHSA-cfp8-93x2-6h9x](https://github.com/open5gs/open5gs/security/advisories/GHSA-cfp8-93x2-6h9x) | **7.5** | Open5GS AMF | UserLocationInformation이 누락된 InitialUEMessage 처리 시 RAN-UE 컨텍스트가 해제되지 않아 `ran_ue_pool` 고갈 (DoS) |
| 🟠 High | [CVE-2026-10157](https://nvd.nist.gov/vuln/detail/CVE-2026-10157) | **7.3** | Open5GS AMF | NGAP PathSwitchRequest 핸들러의 부적절한 인증 (Improper Authentication) |
| 🟠 High | [CVE-2026-44473](https://nvd.nist.gov/vuln/detail/CVE-2026-44473) | **7.1** | Ella Core | 위조된 PDUSessionResourceSetupResponse의 SCTP 연결 검증 누락으로 공격자 RAN 방향 GTP 터널 생성 |
| 🟠 High | [CVE-2026-42081](https://nvd.nist.gov/vuln/detail/CVE-2026-42081) | **7.1** | free5GC AMF | PathSwitchRequest의 UE Security Capabilities 미검증으로 핸드오버 지속 DoS (TS 33.501 위반) |
| 🟡 Medium | [CVE-2026-8743](https://nvd.nist.gov/vuln/detail/CVE-2026-8743) | **6.3** | Open5GS AMF | `ran_ue_find_by_amf_ue_ngap_id`의 부적절한 인가 (Improper Authorization) |
| 🟡 Medium | [CVE-2026-44475](https://nvd.nist.gov/vuln/detail/CVE-2026-44475) | **6.1** | Ella Core | 악성 gNB의 PathSwitchRequest로 저장된 UE Security Capabilities 덮어쓰기 |
| 🟡 Medium | [GHSA-mg8r-2cvv-xq9j](https://github.com/open5gs/open5gs/security/advisories/GHSA-mg8r-2cvv-xq9j) | **5.4** | Open5GS AMF | 다른 gNB 연결이 소유한 UE 컨텍스트를 UEContextReleaseRequest로 해제 가능 (Cross-association release) |
| 🟢 Low | [CVE-2026-14618](https://nvd.nist.gov/vuln/detail/CVE-2026-14618) | **4.3** | Open5GS AMF | `amf_nnrf_handle_nf_discover` 처리 결함으로 인한 DoS |
| 🟢 Low | [CVE-2026-44474](https://nvd.nist.gov/vuln/detail/CVE-2026-44474) | **3.7** | Ella Core | NAS Security Mode Command와 N2 핸드오버 동시 수행 시 KgNB 불일치로 핸드오버 실패 |
| 🟢 Low | [CVE-2026-42082](https://nvd.nist.gov/vuln/detail/CVE-2026-42082) | **3.7** | free5GC AMF | 동시 보안 절차 규칙(TS 33.501 §6.9.5.1) 미적용으로 NAS/AS 보안 컨텍스트 불일치 |
| 🟢 Low | [CVE-2026-10565](https://nvd.nist.gov/vuln/detail/CVE-2026-10565) | **3.1** | Open5GS AMF | `gmm_state_security_mode` (NGAP Handover) 경쟁 조건 (Race Condition) |

<details>
<summary>📌 References</summary>

- [Open5GS Security Advisories](https://github.com/open5gs/open5gs/security/advisories)
- [free5GC](https://github.com/free5gc/free5gc) · [Ella Core](https://github.com/ellanetworks/core)
- [NVD – National Vulnerability Database](https://nvd.nist.gov/)
- CVSS 점수는 NVD 또는 GitHub Security Advisory에 등록된 값을 기준으로 하며, 평가 기관에 따라 점수가 다를 수 있습니다.

</details>

---

<div align="center">
<sub>Last updated: 2026-10</sub>
</div>
