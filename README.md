# SENV

## Development status: issue #1

The repository now includes an offline, resettable mock enterprise sandbox.
It supplies typed contracts, synthetic SQL/RAG/file/memory data, captured email and
webhook effects, and deterministic benign/attack scenarios. The production gateway
and remaining security layers are planned, not implemented in this first slice.

### Run locally

Install Python 3.11 or newer, clone this repository, and open a terminal in its root:

```sh
python -m unittest discover -v
python -m senv
```

No pip install, Docker, API keys, environment variables, or network connection is
needed. The CLI emits JSON evidence for eight scenario/mode combinations and exits
nonzero if an effect oracle fails. Each scenario starts from fresh in-memory state;
rerunning the command resets everything. In Python, use `with Sandbox() as target`
from `senv.sandbox` and `target.reset()` to reset an existing fixture.

Read the [document index and implementation handoff](documents/README.md) for report
links, acceptance coverage, known limitations, and the corrected GitHub issue map.
AI contributors should also read [the model handoff](READ_ME_IF_YOU_ARE_AN_AI_MODEL.md).

## Project vision

[SENV] is a modular runtime security gateway designed to protect enterprise AI agent workflows from indirect prompt injection, privileged tool misuse, and data exfiltration without altering underlying foundation models. Sitting as a protective middleware between autonomous agents and enterprise execution environments (databases, APIs, and file systems), [SENV] intercepts privileged actions before execution. It evaluates proposed tool calls through deterministic capability policies and dual-execution behavioral validation to detect state hijacking and context poisoning in real time. By pairing runtime interception with an automated, graph-based adversarial red-teaming engine, the platform establishes provable runtime safety boundaries for multi-agent enterprise deployments.

---

## Team Members
* **[Arda Yüksel]**
* **[Atilla Akkuş]**
* **[Atilla Ündar]** 
* **[Gökdeniz Derelioğlu]** 
* **[Musa Qureshi]** 

## Project Information
* **Supervisor:** Prof. Mohammad Mahmoody
* **Innovation Expert:** Erhan Dolak

## Course Deliverables
* [CS 491 - Project Information Form](docs/SENV_Project_Information_Form.pdf)
* [Analysis Report](documents/reports/01_SENV_Requirements_and_Analysis.pdf)
* [Architecture and Design Report](documents/reports/02_SENV_Architecture_and_Design.pdf)
* [All reports and implementation notes](documents/README.md)

## Repositories
* *(Links coming soon)*
