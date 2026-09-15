# Awesome AI for Hacking & Cybersecurity

> Lista curada y fusionada de agentes, herramientas, frameworks, modelos, datasets, benchmarks, papers y recursos de aprendizaje sobre **Inteligencia Artificial aplicada al hacking, pentesting y la ciberseguridad** (ofensiva y defensiva), y sobre la **seguridad de los propios sistemas de IA** (LLMs, agentes, RAG, MCP).

## ⚠️ Uso Responsable

Todo el material de este repositorio es para **fines educativos y de testing de seguridad autorizado únicamente**. No se proveen instrucciones para acceso no autorizado, evasión de protecciones en sistemas de terceros, despliegue de malware o suplantación de identidad. Si no puedes demostrar autorización explícita sobre un objetivo, no lo pruebes: usa un laboratorio, un benchmark o una aplicación intencionalmente vulnerable.

Para divulgación responsable, consulta la [OWASP Vulnerability Disclosure Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Vulnerability_Disclosure_Cheat_Sheet.html) y [CERT/CC](https://www.sei.cmu.edu/about/divisions/cert/index.cfm).

**Leyenda de tipo** 🟢 público/open-source · 🔬 investigación (paper/benchmark/dataset) · 🟠 comercial con componentes abiertos · ⚠️ licencia restrictiva, no comercial o poco clara — revisar antes de usar.

## 📋 Índice

1. [Fundamentos, Gobernanza y Marcos de Referencia](#1-fundamentos-gobernanza-y-marcos-de-referencia)
2. [Seguridad de Sistemas de IA (Security FOR AI)](#2-seguridad-de-sistemas-de-ia-security-for-ai)
3. [IA para Seguridad Ofensiva (Pentest & Red Team)](#3-ia-para-seguridad-ofensiva-pentest--red-team)
4. [AppSec y Vulnerability Research con IA](#4-appsec-y-vulnerability-research-con-ia)
5. [AI/ML Supply Chain y Seguridad de Modelos](#5-aiml-supply-chain-y-seguridad-de-modelos)
6. [Threat Intelligence, SOC/SIEM y DFIR con IA](#6-threat-intelligence-socsiem-y-dfir-con-ia)
7. [Modelos de IA Especializados en Ciberseguridad](#7-modelos-de-ia-especializados-en-ciberseguridad)
8. [Datasets para Entrenamiento y Evaluación](#8-datasets-para-entrenamiento-y-evaluación)
9. [Benchmarks, Cyber Ranges y Marcos de Evaluación](#9-benchmarks-cyber-ranges-y-marcos-de-evaluación)
10. [Sandboxing de Agentes de IA](#10-sandboxing-de-agentes-de-ia)
11. [OSINT, Cloud/IaC y Phishing con IA](#11-osint-cloudiac-y-phishing-con-ia)
12. [Machine Learning "Clásico" aplicado a Seguridad (pre-LLM)](#12-machine-learning-clásico-aplicado-a-seguridad-pre-llm)
13. [Papers de Investigación](#13-papers-de-investigación)
14. [Libros y Publicaciones](#14-libros-y-publicaciones)
15. [Cheatsheets y Guías](#15-cheatsheets-y-guías)
16. [Certificaciones y Cursos](#16-certificaciones-y-cursos)
17. [Eventos y Conferencias](#17-eventos-y-conferencias)
18. [Observabilidad y Monitoreo de LLMs](#18-observabilidad-y-monitoreo-de-llms)
19. [Podcasts, YouTube, Blogs y Referentes](#19-podcasts-youtube-blogs-y-referentes)
20. [Otras Listas Awesome Relacionadas (IA + Seguridad)](#20-otras-listas-awesome-relacionadas-ia--seguridad)
21. [Apéndice: Listas Generales de Hacking (no específicas de IA)](#21-apéndice-listas-generales-de-hacking-no-específicas-de-ia)

---

## 1. Fundamentos, Gobernanza y Marcos de Referencia

Vocabulario compartido, marcos de gestión de riesgo y taxonomías de amenaza para razonar sobre IA + seguridad antes de elegir una herramienta.

- **OWASP GenAI Security Project / OWASP Top 10 for LLM Apps (2025)** — guía activa de OWASP para riesgos de LLM y aplicaciones GenAI (LLM01–LLM10, incluyendo System Prompt Leakage, Vector/Embedding Weaknesses, Misinformation, Unbounded Consumption). https://genai.owasp.org/ · https://owasp.org/www-project-top-10-for-large-language-model-applications/
- **OWASP ML Top 10** — los 10 riesgos de seguridad de machine learning identificados por OWASP. https://owasp.org/www-project-machine-learning-security-top-10/
- **OWASP AI Security and Privacy Guide** — guía amplia de seguridad y privacidad para diseño, despliegue y operación de sistemas de IA. https://owasp.org/www-project-ai-security-and-privacy-guide/
- **OWASP AI Security Solutions Landscape** — guía de referencia sobre riesgos clave y controles críticos para asegurar LLMs y aplicaciones GenAI. https://genai.owasp.org/ai-security-solutions/
- **OWASP Top 10 2025 (general)** — actualizado con A03: Software Supply Chain Failures y A10: Mishandling of Exceptional Conditions. https://owasp.org/Top10/
- **OWASP AI Security Verification Standard (AISVS)** 🔬⚠️ — estándar de verificación con requisitos de seguridad testeables para aplicaciones de IA (ciclo de vida del modelo, supply chain, datos, sistemas agénticos, integraciones MCP). Nota: licencia compartida CC BY-SA. https://github.com/OWASP/AISVS
- **OWASP Agentic SAMM (asamm)** 🔬 — extensión de OWASP SAMM para desarrollo impulsado por IA: taxonomía de amenazas por punto de entrada + 17 controles en 5 funciones SAMM (Governance, Design, Implementation, Verification, Operations), con madurez L1/L2/L3. Licencia CC BY-SA 4.0. (CyberOK / S. Gordeychik) https://github.com/scadastrangelove/asamm
- **NIST AI Risk Management Framework (AI RMF) + GenAI Profile** — framework voluntario organizado en Govern, Map, Measure y Manage. https://www.nist.gov/itl/ai-risk-management-framework
- **NIST AIRC** — NIST Trustworthy & Responsible AI Resource Center. https://airc.nist.gov/Home
- **NCSC Secure AI System Development** — guía de ciclo de vida (diseño, desarrollo, despliegue, operación/mantenimiento) para sistemas de IA seguros. https://www.ncsc.gov.uk/collection/guidelines-secure-ai-system-development
- **MITRE ATLAS** — base de conocimiento viva de amenazas a sistemas habilitados por IA (TTPs modelados sobre ATT&CK). https://atlas.mitre.org/
- **MITRE ATT&CK** — base de conocimiento general de comportamiento adversario que complementa a ATLAS. https://attack.mitre.org/
- **CISA AI Guidelines / AI Security Best Practices** — guía conjunta para sistemas de IA/ML. https://www.cisa.gov/ai
- **ENISA Multilayer Framework for Good Cybersecurity Practices for AI** — framework de buenas prácticas de ciberseguridad para IA. https://www.enisa.europa.eu/publications/multilayer-framework-for-good-cybersecurity-practices-for-ai
- **AI Incident Database** — casos documentados de incidentes de IA para ejercicios de gobernanza y descubrimiento de riesgos. *(recurso citado por la fuente `Awesome-Hacking-with-AI`, sin URL propia en el material original)*
- **AVID Taxonomy** — vocabulario estructurado para identificación y documentación de riesgos de IA. *(sin URL propia en el material original)*
- **MLSecOps Top 10 / The MLSecOps Top 10** — prácticas de seguridad top para operaciones de machine learning. https://ethical.institute/security.html
- **NIST Adversarial ML Taxonomy** — terminología compartida para amenazas y mitigaciones de ML adversario. *(sin URL propia en el material original)*
- **OWASP WrongSecrets LLM exercise** — ejercicio práctico para testear la seguridad de un modelo de IA. https://wrongsecrets.herokuapp.com/challenge/32

---

## 2. Seguridad de Sistemas de IA (Security FOR AI)

Una aplicación de IA es más que un modelo: prompts, fuentes de recuperación, vector stores, identidades, definiciones de herramientas, rutas de ejecución de código, logs, memoria, infraestructura de despliegue y usuarios forman parte del perímetro de seguridad.

### 2.1 LLM, RAG y Seguridad de Agentes — Frameworks y Guías

- **Promptfoo** 🟢 — CLI y librería open-source (MIT) para evaluación y red-teaming de LLMs, agentes y RAG; 50+ plugins de ataque, adaptativo multi-turno (PAIR, tree-of-attacks, crescendo); usado por 250k+ desarrolladores. Nota: OpenAI anunció un acuerdo de adquisición en marzo de 2026; sigue licenciado MIT. https://github.com/promptfoo/promptfoo
- **garak** 🟢 — el escáner de vulnerabilidades de LLM de NVIDIA; prueba 120+ categorías (alucinación, fuga de datos, prompt injection, desinformación, toxicidad, jailbreaks). (NVIDIA) https://github.com/NVIDIA/garak
- **PyRIT** 🟢 — Python Risk Identification Tool para IA generativa (Microsoft), framework de automatización de red-teaming con orquestación multi-turno; usado en 100+ operaciones reales. https://github.com/microsoft/PyRIT
- **Purple Llama** 🟢 — clasificadores Llama Guard, CodeShield y CyberSecEval de Meta. https://github.com/meta-llama/PurpleLlama
- **FuzzyAI** 🟠 — framework de fuzzing automatizado de LLM para identificar jailbreaks y vulnerabilidades. (CyberArk) https://github.com/cyberark/FuzzyAI
- **Open-Prompt-Injection** 🟢🔬 — toolkit y benchmark open-source para implementar y evaluar ataques y defensas de prompt injection. (Yupei Liu et al.) https://github.com/liu00222/Open-Prompt-Injection
- **Agentic Radar** 🟠 — escáner CLI de seguridad open-source para workflows agénticos (LangGraph, CrewAI, n8n); mapea flujos de herramientas/datos y marca riesgos. (SplxAI) https://github.com/splx-ai/agentic-radar
- **NVIDIA SkillSpector** 🟢 — escáner de seguridad para skills de agentes de IA usados por Claude Code, Codex CLI, Gemini CLI; combina análisis estático, AST/YARA/taint, revisión semántica LLM opcional, chequeos MCP de mínimo privilegio, scoring de riesgo, salida SARIF/JSON/Markdown. https://github.com/NVIDIA/SkillSpector
- **Agent Threat Rules (ATR)** 🟢 — reglas de detección versionadas y legibles por máquina para amenazas de agentes de IA (prompt injection, tool poisoning, ataques MCP, compromiso de skills) — "Sigma para agentes"; 768 reglas en 10 categorías con integraciones para Microsoft AGT, Cisco AI Defense, MISP, OWASP, FINOS y SigmaHQ. https://github.com/Agent-Threat-Rule/agent-threat-rules
- **OWASP Agent Memory Guard** 🟢 — framework oficial de OWASP para detectar y prevenir memory poisoning en agentes de IA (OWASP ASI06); escanea almacenes de memoria de agentes buscando payloads de prompt injection, manipulación de memoria y exfiltración de datos. https://github.com/OWASP/www-project-agent-memory-guard
- **Semgrep** 🟢 — análisis estático determinístico, compañero de la revisión de código asistida por IA; también base de rulesets específicos (p. ej. detección de código malicioso). https://github.com/semgrep/semgrep
- **Giskard** 🟢 — framework open-source de evaluación, testing y red-teaming para agentes LLM, incluyendo escaneo de vulnerabilidades de agentes y evaluación RAG. (Giskard AI) https://github.com/Giskard-AI/giskard-oss
- **DeepTeam** 🟢 — framework open-source para red-teaming de LLMs y sistemas LLM (jailbreaks, prompt injection, fuga de datos, riesgos de seguridad). https://github.com/confident-ai/deepteam
- **AgentDojo** 🟢🔬 — entorno de benchmark para ataques y defensas de prompt injection en agentes LLM que usan herramientas. https://github.com/ethz-spylab/agentdojo
- **Anthropic-Cybersecurity-Skills** 🟢 — gran librería comunitaria de skills de ciberseguridad para agentes de IA, mapeada a MITRE ATT&CK, NIST CSF, MITRE ATLAS, D3FEND y NIST AI RMF. Nota: proyecto comunitario independiente, no afiliado a Anthropic. https://github.com/mukul975/Anthropic-Cybersecurity-Skills
- **Claude-BugHunter** 🟢 — bundle de skills de Claude Code para bug hunting autorizado y workflows de red-team externo (web, API, identidad, cloud, recon, reporting, Burp MCP, CLI `cbh`). https://github.com/elementalsouls/Claude-BugHunter
- **Agent Security Bench (ASB)** 🟢🔬 — benchmark oficial ICLR 2025 para evaluar ataques y defensas en agentes basados en LLM en diez escenarios (prompt injection directa/indirecta, memory poisoning, estrategias defensivas). https://github.com/agiresearch/ASB
- **Agent3Sigma-Canary** 🟢🔬 — framework de investigación sandboxed para evaluar seguridad de agentes de IA sobre trayectorias de ejecución completas (inyección directa/indirecta, envenenamiento de skills y memoria). (Ant Group) https://github.com/antgroup/Agent3Sigma-Canary
- **Skill-Inject** 🟢🔬 — benchmark para medir vulnerabilidades de prompt injection en archivos de skill de agentes en Claude Code, Codex CLI y Gemini CLI. https://github.com/aisa-group/skill-inject
- **OWASP Agent Security Regression Harness** 🟢 — harness vendor-neutral para ejecutar escenarios repetibles de abuso de agentes/MCP y emitir resultados de regresión legibles por máquina. *(proyecto OWASP Incubator, sin URL específica confirmada en la fuente original)*
- **Semgrep AI Best Practices** — reglas de seguridad para código que integra proveedores LLM, MCP, asistentes y frameworks de agentes. *(sin URL propia confirmada en la fuente original — ver repo general de Semgrep arriba)*

### 2.2 Escáneres y Auditores de Agentes / Skills / MCP

- **agent-audit** 🟢 — auditor forense para agentes de codificación locales (Claude Code, Codex CLI, OpenClaw) y escáner de superficie de proyecto para repos que envían skills/plugins/manifiestos MCP; 296 reglas. (CyberOK / S. Gordeychik) https://github.com/scadastrangelove/agent-audit
- **AI-Infra-Guard** 🟢 — plataforma full-stack de red-teaming de IA: escaneo de seguridad OpenClaw, escaneo de agentes, escaneo de skills, escaneo MCP, escaneo de vulnerabilidades de infraestructura de IA y evaluación de jailbreak LLM. (Tencent Zhuque Lab) https://github.com/Tencent/AI-Infra-Guard
- **Ramparts** 🟢 — escáner en Rust para servidores MCP y bundles de agent-skill; reglas YARA, análisis LLM opcional, lookups OSV/CVE, mapeo a OWASP MCP Top 10. https://github.com/highflame-ai/ramparts
- **mcp-armor** 🟢 — escáner de seguridad MCP local con auto-descubrimiento de configs de IDE agénticos, inventario de herramientas/recursos/prompts, chequeos de prompt injection, detección de rug-pull y tool-poisoning. (Aira Security) https://github.com/aira-security/mcp-armor
- **aguara** 🟢 — escáner estático de un solo binario (Go, sin LLM) para skills de agentes de IA y servidores MCP; motor multi-capa (patrones + NLP + taint tracking + detección de rug-pull). Companion **aguara-mcp** expone el escaneo como herramienta MCP. https://github.com/garagon/aguara · https://github.com/garagon/mcp-aguara
- **agent-scan (Snyk)** 🟢 — escáner de seguridad para agentes de IA, servidores MCP y skills de agente; sucesor del trabajo original de Invariant Labs mcp-scan. https://github.com/snyk/agent-scan
- **inkog** 🟠 — escáner estático de seguridad respaldado comercialmente para agentes de IA en LangChain, LangGraph, CrewAI, AutoGen y workflows no-code; CLI Apache-2.0 con motor de deep-scan propietario. https://github.com/inkog-io/inkog
- **AgentShield** 🟢 — escáner de seguridad para configuraciones de agentes de IA, servidores MCP, hooks y permisos de herramientas, con CLI, GitHub Action y workflows de app. https://github.com/affaan-m/agentshield
- **repo-forensics** 🟢⚠️ — escáner offline para repos de agentes de IA, skills, plugins y servidores MCP; licencia PolyForm Noncommercial. https://github.com/alexgreensh/repo-forensics
- **Cisco AI Defense – skill-scanner** 🟠 — escáner para skills de agentes combinando patrones YAML + YARA, LLM-as-a-judge y análisis de flujo de datos conductual (formatos Codex/Cursor). https://github.com/cisco-ai-defense/skill-scanner
- **Cisco AI Defense – mcp-scanner** 🟢⚠️ — escáner para servidores MCP y superficies de herramientas agénticas: herramientas, prompts, recursos, riesgo de paquetes, indicadores de malware y preparación de despliegue. https://github.com/cisco-ai-defense/mcp-scanner
- **mcp-guardian** 🟢 — librería y CLI JS/TS para detectar prompt injection en descripciones de herramientas MCP y fijar (pin) definiciones de herramientas. https://github.com/alexandriashai/mcp-guardian
- **MCP Observatory** 🟢🟠 — herramienta de testing CI-nativa para servidores MCP: drift de esquema, simulación segura de ataques, verificación record/replay, health scoring y evidencia SARIF. (KryptosAI) https://github.com/KryptosAI/mcp-observatory
- **skilltotal** 🟢 — escáner estático determinístico offline (regex + AST, sin LLM, sin cuenta) para componentes de IA: skills/plugins de agente, servidores MCP, paquetes npm/PyPI y repos git; mapea al OWASP Agentic Skills Top 10 y emite JSON + SARIF 2.1.0. https://github.com/pezhik/skilltotal
- **Sunglasses** 🟢 — escáner local de input/contenido para agentes de IA que revisa prompts, archivos, metadatos multimedia, skills y descripciones de herramientas contra reglas de prompt-injection, exfiltración, inyección de comandos y agent-threat. https://github.com/sunglasses-dev/sunglasses
- **trentclaw** 🟠 — auditor de seguridad client-side para despliegues de OpenClaw: redacción de secretos local, luego sube metadatos y archivos de skill al API de Trent AI, que identifica configuraciones erróneas y skills riesgosas. (Trent AI) https://github.com/trnt-ai/trent-openclaw-security-assessment
- **A2A Security Scanner** 🟢 — escáner CLI/PyPI para agent cards Agent-to-Agent (A2A), código fuente, registros y endpoints en vivo, con validación de especificación, reglas YARA, heurísticas y analizador LLM opcional. (Cisco AI Defense) https://github.com/cisco-ai-defense/a2a-scanner
- **Ship Safe** 🟢🟠 — CLI de seguridad local para código de aplicación, configuración de agentes de IA/MCP, secretos, dependencias, CI y superficies cloud/IaC, con chequeos determinísticos, análisis opcional asistido por IA y salida SARIF. https://github.com/asamassekou10/ship-safe
- **AgentSeal** 🟠⚠️ — CLI de seguridad de agentes y librería runtime para escanear servidores MCP, skills, prompts y configuración, más workflows de guard/monitoreo local con red-teaming opcional asistido por modelo. Licencia FSL-1.1-Apache-2.0 (source-available, no OSI). https://github.com/getagentseal/agentseal
- **SlowMist Agent Security** 🟢 — skill y workflow de revisión de seguridad para auditar skills de agente, servidores MCP, repositorios, URLs y documentos antes de instalación o uso. https://github.com/slowmist/slowmist-agent-security

### 2.3 Protección y Enforcement en Runtime

- **nono** 🟢 — sandbox de mínimo privilegio para agentes de codificación de IA que aísla al agente y a las herramientas delegadas con políticas componibles de filesystem, red, proxy de credenciales y comandos. (NoLabs) https://github.com/nolabs-ai/nono
- **cplt** 🟢 — wrapper de sandbox respaldado por kernel para agentes de codificación de IA; aplica Seatbelt en macOS o Landlock/seccomp en Linux, aprobaciones content-pinned por política de repositorio. (NAV Noruega) *(sin URL confirmada en la fuente original)*
- **Arcjet Guard** 🟢🟠 — guardia runtime en JavaScript para llamadas a herramientas de agentes de IA y handlers MCP, con detección de prompt injection, detección/redacción de datos sensibles y reglas de política local. https://github.com/arcjet/arcjet-js
- **ToolHive** 🟢 — plataforma para ejecutar servidores MCP en contenedores aislados con política de identidad/acceso por request, workflows de registro y gateway, logs de auditoría, soporte de operador Kubernetes. (Stacklok) https://github.com/stacklok/toolhive
- **Pipelock** 🟢 — firewall de agentes de IA y capa de control de egreso verificable que media tráfico HTTP, WebSocket, CONNECT, MCP y A2A para detectar prompt injection, exfiltración de secretos, SSRF y acciones sospechosas de salida. https://github.com/luckyPipewrench/pipelock
- **mcp-context-protector** 🟢 — wrapper de seguridad MCP que se sitúa frente a servidores MCP downstream, escanea respuestas de herramientas con proveedores de guardrail, y soporta workflows de cuarentena/revisión. (Trail of Bits) https://github.com/trailofbits/mcp-context-protector
- **MCP Defender** 🟢⚠️ — app de escritorio que hace proxy de requests/respuestas de tool-call MCP para Cursor, Claude, VS Code y Windsurf, verifica el tráfico interceptado contra firmas. Licencia AGPL-3.0; adquirido por Docker. https://github.com/MCP-Defender/MCP-Defender
- **MCP Gateway** 🟢 — gateway MCP basado en plugins que hace proxy de servidores MCP configurados, sanitiza datos sensibles de request/response, soporta plugins de guardrail (masking básico y Presidio). (Lasso Security) https://github.com/lasso-security/mcp-gateway
- **Parallax** 🟢 — motor de política runtime en Rust para agentes de IA: evalúa eventos del ciclo de vida con reglas regex, keyword, Sigma, CEL y SQL para bloquear o redactar prompt injection, exfiltración de datos, tool calls peligrosos y fuga de secretos. https://github.com/agent-defense/parallax
- **Armorer Guard** 🟢 — escáner y proxy MCP local en Rust para prompt injection, fuga de credenciales, exfiltración y argumentos de tool-call riesgosos en agentes de IA, sin llamadas de red del propio escáner. https://github.com/ArmorerLabs/Armorer-Guard
- **onecli** 🟢 — gateway de credenciales y bóveda cifrada para agentes de IA; inyecta credenciales reales de API en el gateway para que los agentes solo vean claves placeholder. https://github.com/onecli/onecli
- **microsandbox** 🟢 — sandboxes programables local-first respaldados por microVM para agentes de IA, con SDKs, CLI, soporte MCP y aislamiento de hardware rootless. https://github.com/superradcompany/microsandbox
- **agentguard** 🟢 — capa de seguridad en tiempo real para agentes de codificación: hooks que escanean cada skill nueva, bloquean acciones peligrosas antes de ejecutar, patrullas diarias de postura. https://github.com/GoPlusSecurity/agentguard
- **defenseclaw** 🟠 — capa de enforcement y evidencia para despliegues agénticos: chequeos estáticos CodeGuard, sandboxing, ingestión de registro con guardas SSRF, y auditoría/observabilidad. (Cisco AI Defense) https://github.com/cisco-ai-defense/defenseclaw
- **clawsec** 🟢⚠️ — suite de skills de seguridad para agentes de la familia OpenClaw; licencia AGPL-3.0. (Prompt Security) https://github.com/prompt-security/clawsec
- **AgentLock** 🟢🔬⚠️ — puerta de autorización pre-acción para tool calls de agentes LLM que decide por proveniencia de sesión en lugar de contenido, con permisos deny-by-default, recibos firmados Ed25519 y log de auditoría hash-chained. Licencia AGPL-3.0 con opciones comerciales. https://github.com/webpro255/agentlock
- **h5i** 🟢 — CLI local en Rust para workspaces auditables de agentes de codificación: worktrees por agente con políticas de sandbox, captura de proveniencia, revisión por pares, señales de auditoría de secretos/prompt-injection. https://github.com/h5i-dev/h5i
- **DvalinCode** 🟢 — agente de codificación de IA local-first con controles de gobernanza runtime: puertas de política org/repo para herramientas, modelos, servidores MCP, rutas y comandos. https://github.com/arthurpanhku/dvalincode
- **TAP** 🟢🟠 — proxy de aislamiento de credenciales y servidor MCP para agentes de IA: los agentes envían credenciales placeholder, TAP inyecta secretos reales server-side tras chequeos de política por acción. (human.tech) https://github.com/holonym-foundation/tap-oss
- **Agent Memory Guard (Runtime)** 🟢 — middleware runtime para lecturas/escrituras de memoria de agentes de IA, filtrando prompt injection, memory poisoning, fuga de secretos/PII, manipulación de claves protegidas y anomalías de tamaño antes de reutilizar memoria persistida. (OWASP) https://github.com/OWASP/www-project-agent-memory-guard
- **AIO Sandbox** 🟢⚠️ — workspace Docker todo-en-uno para agentes de IA con navegador, shell, archivos, ejecución de código, MCP e interfaces VSCode server. https://github.com/agent-infra/sandbox
- **Agentgateway** 🟢 — proxy y gateway agent-native para tráfico MCP y A2A con autenticación OAuth/JWT/API-key, políticas RBAC basadas en CEL, TLS, rate limiting y observabilidad OpenTelemetry. https://github.com/agentgateway/agentgateway
- **Kubernetes Agent Sandbox** 🟢 — CRDs y controladores de Kubernetes para workloads de agente singleton aislados y con estado, delegando el aislamiento de bajo nivel a runtimes configurados como gVisor o Kata Containers. (Kubernetes SIG Apps) https://github.com/kubernetes-sigs/agent-sandbox
- **Prismor** 🟢 — plano de control runtime self-hosted para agentes de codificación con hooks pre-tool-call, decisiones observe/approve/block basadas en política, gateway MCP y controles de secretos/egreso. https://github.com/PrismorSec/prismor
- **tirith** 🟢⚠️ — guardia de terminal para desarrolladores y agentes de codificación de IA que intercepta trucos de homógrafos e inyección de terminal, cadenas de ejecución ofuscadas y exfiltración de credenciales. Licencia AGPL-3.0. https://github.com/sheeki03/tirith
- **ADR (Agentic AI Detection and Response)** 🟢🔬 — sistema que combina telemetría de agentes cross-cliente, escenarios de seguridad ADR-Bench y un detector dual-agente para intención sospechosa, uso de herramientas y trazas de ejecución. (Uber) https://github.com/uber/ADR
- **xaidr** 🟢 — sensor de seguridad runtime in-process para agentes de IA que inspecciona input, tool calls, output y sobres agent-to-agent dentro del proceso del agente. (Delphi Security) https://github.com/delphisecurity/xaidr
- **Agentmetry** 🟢 — flight recorder local-first para agentes de codificación de IA y servidores MCP que escribe un rastro JSONL hash-chained con raíces Merkle RFC 6962. https://github.com/blitzcrieg1/agentmetry
- **piighost** 🟢 — capa de pseudonimización runtime local que reemplaza PII detectada con placeholders estables antes de llamadas al modelo y restaura los valores originales en respuestas. https://github.com/Athroniaeth/piighost
- **HOL Guard** 🟢🟠 — capa de seguridad runtime local-first para agentes de codificación que evalúa comandos, instalaciones de paquetes, skills, configuración MCP y acciones sensibles mediante política, aprobación, evidencia y auditoría. (Hashgraph Online) https://github.com/hashgraph-online/hol-guard
- **StackOne Defender** 🟢 — guardia runtime offline en TypeScript para prompt injection indirecta en resultados de herramientas, usando clasificadores ONNX empaquetados, chequeos determinísticos y sanitización. https://github.com/StackOneHQ/defender
- **Earl** 🟢 — proxy de capacidades para agentes de IA que expone nombres de operación aprobados manteniendo plantillas de request y credenciales fuera del modelo, con política HCL, auditoría y controles de egreso. (Mathematic) https://github.com/mathematic-inc/earl
- **Portkey AI Gateway** 🟢🟠 — gateway de IA abierto con ruteo de proveedor, controles de fallback/retry, integraciones de guardrail, observabilidad y soporte de tráfico MCP. https://github.com/Portkey-AI/gateway
- **Casbin AI Gateway** 🟢 — gateway local y capa de política para tráfico de proveedor de modelo y MCP, combinando mediación de claves de proveedor, control de acceso y registros de prompts. (Apache Casbin) https://github.com/apache/casbin-gateway
- **Sandlock** 🟢 — sandbox de proceso Linux sin privilegios usando Landlock, seccomp-BPF y notificación de usuario seccomp para aplicar políticas de filesystem, red, syscall y ejecución por proceso. (Multikernel) *(mencionado en la fuente sin URL propia confirmada — ver referencias generales de sandboxing en la sección 10)*
- **emisar** 🟠⚠️ — plano de control de infraestructura de agentes que expone acciones declaradas y tipadas vía MCP, aplica política y puertas de aprobación antes del despacho. https://github.com/AndrewDryga/emisar
- **Gram** 🟢🟠⚠️ — stack open-source detrás del control plane de IA de Speakeasy; gestiona MCPs, Skills y Assistants con permisos granulares. Licencia AGPL-3.0. *(sin URL propia confirmada en la fuente original)*
- **sofagent** 🟢 — suite de auditoría y gobernanza commit-time para agentes de codificación de IA que escanea diffs de git contra reglas determinísticas y registra historial de auditoría local. *(sin URL propia confirmada en la fuente original)*
- **Norviq** 🟢 — punto de enforcement de política Kubernetes para tool calls de agentes LLM que fija (pin) cada definición de herramienta por hash de contenido en el descubrimiento y evalúa cada `tools/call` contra política OPA/Rego. *(sin URL propia confirmada en la fuente original)*
- **Lunar** 🟢🟠 — gateway API y MCP que combina visibilidad de tráfico saliente, enforcement de política, límites de tasa, retries, circuit breakers y agregación centralizada de servidores MCP. (Lunar.dev) *(sin URL propia confirmada en la fuente original)*
- **Adrian** 🟢🟠 — capa de monitoreo e intervención runtime que correlaciona acciones de agentes con trazas de razonamiento disponibles, vía SDKs Python/TypeScript e integración con Claude Code. (Secure Agentics) *(sin URL propia confirmada en la fuente original)*

### 2.4 Seguridad de MCP (Model Context Protocol)

El Model Context Protocol (MCP) estandariza cómo hosts, clientes y servidores exponen recursos, prompts y herramientas a sistemas de IA. Las herramientas son fronteras de seguridad: pueden acceder a datos o causar acciones.

- **MCP Specification** — conceptos canónicos y principios de confianza/seguridad para recursos, prompts, herramientas, autorización e interacción de usuario. https://modelcontextprotocol.io/
- **MCP-Security-Checklist** 🟢 — checklist de seguridad para clientes MCP, servidores, despliegues multi-MCP, controles de ciclo de vida, authz/authn, aislamiento e integraciones MCP específicas de cripto. (SlowMist) https://github.com/slowmist/MCP-Security-Checklist
- **Lasso MCP Gateway** 🟢 — primera solución open-source centrada en seguridad para Model Context Protocol; gateway MCP con sanitización de datos sensibles y chequeo de reputación/riesgo de servidor. (Lasso Security) https://github.com/lasso-security/mcp-gateway
- **Awesome MCP Security** — directorio complementario de recursos, herramientas, investigación y guías de seguridad MCP. https://github.com/Puliczek/awesome-mcp-security
- **MCP_Security (ORKL)** 🟢⚠️ — servidor MCP para consultar el API de threat-intel ORKL. (fr0gger) https://github.com/fr0gger/MCP_Security
- **Google Security Operations and Threat Intelligence MCP Server** 🟢 — servidores y paquetes MCP que permiten a clientes MCP acceder a Google Security Operations, SOAR, Google Threat Intelligence y Security Command Center. (Google Cloud) https://github.com/google/mcp-security
- **MCP Security Hub** 🟢 — colección de servidores MCP Dockerizados que exponen herramientas ofensivas como Nmap, Nuclei, SQLMap, Ghidra y Hashcat a asistentes con capacidad MCP. (FuzzingLabs) https://github.com/FuzzingLabs/mcp-security-hub
- **Burp Suite MCP Server** 🟢⚠️ — extensión oficial de Burp Suite que expone Burp a clientes de IA vía MCP. Licencia GPL-3.0. (PortSwigger) https://github.com/PortSwigger/mcp-server

### 2.5 AI Red Teaming, Adversarial ML y Benchmarks de Ataque/Defensa

- **Adversarial Robustness Toolbox (ART)** 🟢 — librería insignia de seguridad de machine learning para evaluar y defender modelos contra evasión, envenenamiento, extracción e inferencia en los principales frameworks de ML. (LF AI & Data / IBM) https://github.com/Trusted-AI/adversarial-robustness-toolbox
- **HEART** 🟢 — extensión endurecida de ART para workflows de Test & Evaluation. (IBM) https://github.com/IBM/heart-library
- **Foolbox** 🟢 — toolbox clásico en Python para generar ejemplos adversarios y benchmarking de robustez de modelos PyTorch, TensorFlow y JAX. https://github.com/bethgelab/foolbox
- **CleverHans** 🟢 — librería para generar ejemplos adversarios y hacer benchmarking de defensas. *(sin URL propia confirmada en la fuente original — repo histórico cleverhans-lab/cleverhans)*
- **Counterfit** 🟢 — capa de automatización de Microsoft para evaluar/atacar la seguridad de sistemas de machine learning; también descrita como herramienta de pentesting ML/IA. https://github.com/Azure/counterfit
- **TextAttack** 🟢🔬 — framework Python para ataques adversarios, aumento de datos y entrenamiento para modelos NLP; útil para robustez más allá de escáneres LLM de solo chat. https://github.com/QData/TextAttack
- **Deep-pwning / deep-pwning** 🟢🔬 — framework histórico "Metasploit para machine learning" para experimentar con robustez adversaria de modelos ML. https://github.com/cchio/deep-pwning
- **DeepFool** 🟢 — método simple pero preciso para generar ejemplos adversarios contra redes neuronales profundas. https://github.com/lts4/deepfool
- **AI Red Teaming Playground Labs (AI-Red-Teaming-Playground-Labs)** 🟢 — labs de entrenamiento CTFd para red-team de IA. (Microsoft) https://github.com/microsoft/AI-Red-Teaming-Playground-Labs
- **RAMPART** 🟢 — framework pytest-native para testing de seguridad y safety de aplicaciones de IA agénticas. (Microsoft) https://github.com/microsoft/RAMPART
- **HarmBench** 🟢🔬 — framework de evaluación estandarizado ICML 2024 para red-teaming automatizado y benchmarking de rechazo robusto. (Center for AI Safety) https://github.com/centerforaisafety/HarmBench
- **JailbreakBench** 🟢🔬 — benchmark abierto NeurIPS 2024 de robustez y leaderboard para generar y defenderse de jailbreaks de LLM. https://github.com/JailbreakBench/jailbreakbench
- **AI-Infra-Guard** — ver sección 2.2 (plataforma full-stack que incluye evaluación de jailbreak LLM). https://github.com/Tencent/AI-Infra-Guard
- **AgentDojo** — ver sección 2.1 (benchmark de prompt injection en agentes). https://github.com/ethz-spylab/agentdojo

### 2.6 Guardrails, Detección de Prompt Injection y Jailbreak

- **NeMo Guardrails** 🟢 — guardrails programables (input/output/diálogo/retrieval/ejecución) para apps LLM. (NVIDIA) https://github.com/NVIDIA/NeMo-Guardrails · https://github.com/NVIDIA-NeMo/Guardrails
- **Guardrails AI** 🟢 — framework Python para agregar guards de input/output, validadores y controles de salida estructurada a aplicaciones LLM, con checks de Guardrails Hub. https://github.com/guardrails-ai/guardrails
- **LLM Guard** 🟢 — suite de escáneres de input/output (PII, prompt injection, etc.). Archivado por el mantenedor; retenido como referencia histórica. (Protect AI) https://github.com/protectai/llm-guard
- **Rebuff** 🟢 — detector de prompt injection auto-endurecido (heurísticas + LLM + vector DB + canary tokens). Archivado por el mantenedor. (Protect AI) https://github.com/protectai/rebuff
- **LangKit** 🟢 — toolkit de monitoreo de LLM que extrae señales de seguridad como similitud de jailbreak, similitud de prompt-injection, chequeos de alucinación, patrones PII, toxicidad y métricas de rechazo. (WhyLabs) https://github.com/whylabs/langkit
- **LLM Warden** 🟢 — detección simple de jailbreak (modelo Hugging Face). (jackhhao) https://github.com/jackhhao/llm-warden
- **Vigil** 🟢🔬 — librería/API REST modular (vectores, YARA, transformers) para escanear prompts y respuestas buscando prompt injection. (deadbits) https://github.com/deadbits/vigil-llm
- **LLAMATOR** 🟢⚠️ — framework de red-teaming para chatbots y sistemas GenAI; licencia CC BY-NC-SA 4.0. https://github.com/LLAMATOR-Core/llamator
- **EasyJailbreak** 🟢🔬 — framework para construir y testear prompts de jailbreak adversarios. https://github.com/EasyJailbreak/EasyJailbreak
- **GPTFuzz** 🟢🔬 — framework de investigación para red-teaming de LLMs con prompts de jailbreak autogenerados. https://github.com/sherdencooper/GPTFuzz
- **llm-attacks (GCG)** 🟢🔬 — implementación canónica del ataque de sufijo adversario Greedy Coordinate Gradient para ataques transferibles a modelos de lenguaje alineados. https://github.com/llm-attacks/llm-attacks
- **nanoGCG** 🟢 — implementación PyTorch rápida y liviana del algoritmo de sufijo adversario GCG. https://github.com/GraySwanAI/nanoGCG
- **PINT Benchmark** 🟢🔬 — benchmark de test de prompt-injection para evaluar detectores y guardrails en escenarios multilingües de inyección, jailbreak, benignos y hard-negative. (Lakera) https://github.com/lakeraai/pint-benchmark
- **PIArena** 🟢🔬 — toolbox y benchmark ACL 2026 para ataques y defensas de prompt injection, con ataques/defensas listos para usar, pipelines de evaluación y leaderboard. https://github.com/sleeepeer/PIArena
- **Whistleblower** 🟢⚠️ — herramienta de testing ofensivo para inferir system prompts y descubrir capacidades de aplicaciones LLM expuestas vía APIs. (Repello AI) https://github.com/Repello-AI/whistleblower
- **LLMmap** 🟢🔬 — herramienta de fingerprinting de consulta mínima para identificar LLMs a partir de trazas de comportamiento. https://github.com/pasquini-dario/LLMmap
- **llm-security** 🔬 — PoC original de ataques de prompt injection indirecta. https://github.com/greshake/llm-security
- **JailbreakLLMs** 🔬⚠️ — dataset de investigación de 6,387 prompts de ChatGPT, incluyendo jailbreaks reales de Reddit, Discord y sitios web. https://github.com/TrustAIRLab/JailbreakLLMs
- **In-The-Wild Jailbreak Prompts Dataset** — 15,140 prompts con 1,405 prompts de jailbreak de Reddit, Discord y sitios web (2022–2023). https://huggingface.co/datasets/TrustAIRLab/in-the-wild-jailbreak-prompts
- **JailBreakV-28K** — 28,000 casos de test de jailbreak para MLLMs (20K basados en texto, 8K en imagen). https://huggingface.co/datasets/JailbreakV-28K/JailBreakV-28k
- **Forbidden Question Set** — dataset curado de preguntas prohibidas en categorías de alto riesgo. https://huggingface.co/datasets/TrustAIRLab/forbidden_question_set
- **Do-Not-Answer** 🟢🔬 — dataset para evaluar salvaguardas de LLM en prompts inseguros o sensibles. https://github.com/Libr-AI/do-not-answer
- **prompt-injection-defenses** 🟢⚠️ — catálogo curado de defensas prácticas contra prompt injection. https://github.com/tldrsec/prompt-injection-defenses
- **little-canary** 🟢🔬 — sensor de preflight de riesgo de prompt-injection que enruta input no confiable a través de un modelo sacrificial sin poder, y devuelve pass/flag/block antes de que actúe el agente principal. https://github.com/hermes-labs-ai/little-canary
- **Kiji Privacy Proxy** 🟢 — proxy de privacidad local para tráfico API de IA compatible con OpenAI que detecta y enmascara 26 tipos de PII con un modelo ONNX antes de reenviar requests. (Dataiku 575 Lab) https://github.com/Dataiku/kiji-proxy
- **Anamorpher** 🟢🔬 — herramienta de investigación con frontend y API Python para crear y visualizar ataques de escalado de imagen que revelan prompt injections ocultos en sistemas de IA multimodal. (Trail of Bits) *(sin URL propia confirmada en la fuente original)*
- **Prompt SIREN** 🟢🔬 — workbench de investigación para desarrollar y evaluar ataques y defensas de prompt injection con control de agente por máquina de estados, integraciones AgentDojo/SWE-bench. (Meta AI) *(sin URL propia confirmada en la fuente original)*
- **Argus** 🟢🔬 — framework de red-team black-box para aplicaciones y agentes LLM con adaptadores de objetivo, probes de ataque, juicio determinístico y asistido por modelo, y reportes SARIF/JUnit/HTML/JSON. *(sin URL propia confirmada en la fuente original)*
- **Cryptex OSS** 🟢🟠 — workbench de prompts adversarios basado en navegador y auto-hospedable, con pipelines de transformación, workflows de campaña, métodos TAP/PAIR/Crescendo. *(sin URL propia confirmada en la fuente original)*
- **API Relay Audit** 🟢⚠️ — CLI de auditoría local para relays y proxies de LLM de terceros, testeando prompt injection, sustitución de modelo, reescritura de tool-call. *(sin URL propia confirmada en la fuente original)*
- **AIDR Bastion** 🟢🟠⚠️ — servicio de protección de input runtime que combina reglas de detección, búsqueda por similitud, clasificadores, análisis LLM opcional y chequeos orientados a código. (SOC Prime) *(sin URL propia confirmada en la fuente original)*
- **CaMeL** 🟢🔬 — implementación de investigación de la arquitectura de intérprete CaMeL basada en capacidades, para separar flujo de control confiable de datos no confiables mientras evalúa defensas de prompt-injection en AgentDojo. (Google Research / Google DeepMind / ETH Zürich) *(sin URL propia confirmada en la fuente original)*
- **Meta SecAlign** 🔬⚠️ — código de investigación, receta de entrenamiento y harness de evaluación para modelos Meta SecAlign resistentes a prompt injection. (Meta / UC Berkeley) *(sin URL propia confirmada en la fuente original)*
- **Whistleblower, LLMmap** — ver arriba.
- **ai-prompt-fuzzer** 🟢 — extensión de Burp Suite para fuzzing de prompts GenAI/LLM. (PortSwigger) https://github.com/PortSwigger/ai-prompt-fuzzer
- **spikee** 🟢 — kit de evaluación y explotación de prompt-injection con generación de datasets, integración Burp y jueces conectables. (ReversecLabs/WithSecure) https://github.com/ReversecLabs/spikee
- **promptmap** 🟢⚠️ — escáner de prompt injection para aplicaciones LLM personalizadas en modos white-box y black-box; licencia GPL-3.0. (utkusen) https://github.com/utkusen/promptmap
- **aiapwn** — testing automático de prompt injection con generación de payload a medida. (karimhabush) https://github.com/karimhabush/aiapwn
- **NeuralTrust AI Guide** — guía completa para implementar detección de prompt injection con alertas en tiempo real. https://neuraltrust.ai/
- **PIPE – Prompt Injection Primer** — escenarios de ataque y payloads para ingenieros. (jthack) https://github.com/jthack/PIPE
- **Basic-ML-prompt-injections** — payloads educativos. (Zierax) https://github.com/Zierax/Basic-ML-prompt-injections
- **PayloadsAllTheThings – Prompt Injection** — payloads y bypasses de prompt injection. https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Prompt%20Injection/README.md
- **OWASP LLM Prompt Injection Prevention Cheat Sheet** — cheat sheet y buenas prácticas de prevención. https://cheatsheetseries.owasp.org/cheatsheets/LLM_Prompt_Injection_Prevention_Cheat_Sheet.html
- **Salesforce Prompt Injection Detection Guide** — guía para construir sistemas de IA confiables contra amenazas de prompt injection. https://www.salesforce.com/blog/prompt-injection-detection/
- **NVIDIA AI Red Team Practical Advice** — hallazgos clave de evaluaciones AIRT sobre cómo asegurar aplicaciones impulsadas por IA. https://developer.nvidia.com/blog/practical-llm-security-advice-from-the-nvidia-ai-red-team/
- **Lakera Guard** — detección de prompt injection/jailbreak en tiempo real con alertas casi en tiempo real. (Lakera) https://www.lakera.ai/
- **Prompt Armor** — detección y filtrado en tiempo real de prompts maliciosos. https://promptarmor.com/
- **HiddenLayer AIM Security** — monitoreo de aplicaciones de IA, detección de amenazas en tiempo real y controles de acceso zero-trust. https://hiddenlayer.com/
- **CalypsoAI Moderator** — herramienta comercial con trazas de auditoría, detección de código malicioso y protección contra pérdida de datos. https://www.calypsoai.com/
- **LocalMod** — moderación de contenido self-hosted con detección de prompt injection, toxicidad, PII y NSFW, 100% offline. (KOKOSde) https://github.com/KOKOSde/localmod
- **CircleGuardBench** 🟢 — benchmark completo para evaluar las capacidades de protección de modelos de IA. https://github.com/whitecircle-ai/circle-guard-bench
- **SecLens** 🟢🔬 — benchmark para evaluar LLMs en detección de vulnerabilidades de seguridad usando CVEs reales, cubriendo 406 tareas en 5 lentes de stakeholder y 35 dimensiones de scoring. https://github.com/mattersec-labs/seclens
- **rebuff (langkit / StringSifter)** — ver entradas relacionadas arriba y en sección de fuzzing.
- **Guardrail.ai** — paquete Python para agregar garantías de estructura, tipo y calidad a las salidas de LLMs. https://shreyar.github.io/guardrails/

### 2.7 Modelos Clasificadores de Prompt Injection

- **Wolf Defender Prompt Injection** — modelo de clasificación de texto en Hugging Face para detección de prompt injection en agentes, chatbots y workflows CI. Licencia Apache-2.0. (Patronus Studio / Casdo Labs) *(sin URL propia confirmada en la fuente original — ver Hugging Face)*
- **DeBERTa v3 Prompt Injection v2** — clasificador de prompt injection licenciado Apache-2.0, usable vía pipelines de Transformers y ONNX. (Protect AI) *(sin URL propia confirmada en la fuente original — ver Hugging Face `protectai`)*
- **PromptGuard (CodeIntegrity AI)** ⚠️ — clasificador de prompt-injection y jailbreak basado en ModernBERT. Licencia Apache-2.0, acceso gated automático.
- **Prompt Guard 86M** 🟠⚠️ — clasificador de prompt-injection y jailbreak de Meta, de la familia Llama Guard. Licencia Llama 3.1, acceso gated manual. https://huggingface.co/meta-llama/Prompt-Guard-86M
- **prompt-injection-sentinel** 🔬⚠️ — clasificador ModernBERT-large para detección de prompt-injection y jailbreak. (Qualifire)

### 2.8 Honeypots y Engaño basados en LLM

- **Beelzebub** 🟢⚠️ — honeypot low-code que usa LLMs para simular servicios SSH/HTTP/MCP (Go). Licencia GPL-3.0. https://github.com/mariocandela/beelzebub
- **DECEIVE** 🟢🔬 — honeypot SSH proof-of-concept impulsado por LLM que evalúa sesiones como benignas, sospechosas o maliciosas. (Splunk) *(sin URL propia confirmada en la fuente original)*
- **shelLM** 🟢🔬 — honeypot SSH impulsado por LLM (paper "LLM in the Shell"). *(sin URL propia confirmada en la fuente original)*
- **VelLMes** 🟢🔬 — framework de honeypot LLM multi-protocolo (sucesor de shelLM). *(sin URL propia confirmada en la fuente original)*
- **TRAP** 🟢🔬 — código de investigación para honeypots de Targeted Random Adversarial Prompt que identifican uso de LLM black-box mediante sufijos de prompt específicos del modelo (ACL 2024 Findings). *(sin URL propia confirmada en la fuente original)*
- **llm-honeypot** 🔬⚠️ — honeypot SSH Cowrie extendido con trampas de prompt-injection para detectar agentes hacker LLM. (Palisade Research) *(sin URL propia confirmada en la fuente original)*

---

## 3. IA para Seguridad Ofensiva (Pentest & Red Team)

No existe un "mejor" agente de seguridad universal: la capacidad depende de la tarea, el acceso al objetivo, las herramientas permitidas, el modelo y la supervisión humana.

### 3.1 Agentes de Pentesting Open Source (orden cronológico)

*Tabla original de `Awesome-AI-Hacking-Agents`, con enlaces a GitHub, CodeWiki (documentación generada por Google) y DeepWiki (documentación + chat) cuando existen.*

| # | Nombre | GitHub | CodeWiki | DeepWiki | Fecha | Notas |
|---|---|---|---|---|---|---|
| 1 | AutoPentest-DRL | https://github.com/crond-jaist/AutoPentest-DRL | https://codewiki.google/github.com/crond-jaist/autopentest-drl | https://deepwiki.com/crond-jaist/AutoPentest-DRL | 2021-03-30 | RL profundo para pentesting automatizado |
| 2 | Reaper (Ghost Security) | https://github.com/ghostsecurity/reaper | https://codewiki.google/github.com/ghostsecurity/reaper | https://deepwiki.com/ghostsecurity/reaper | 2022-11-28 | |
| 3 | PentestGPT | https://github.com/GreyDGL/PentestGPT | https://codewiki.google/github.com/greydgl/pentestgpt | https://deepwiki.com/GreyDGL/PentestGPT | 2023-02-27 | USENIX Security 2024; original re-lanzado como pipeline autónomo |
| 4 | hackingBuddyGPT | https://github.com/ipa-lab/hackingBuddyGPT | https://codewiki.google/github.com/ipa-lab/hackingbuddygpt | https://deepwiki.com/ipa-lab/hackingBuddyGPT | 2023-08-02 | Framework mínimo (~50 LOC) para priv-esc Linux y pentesting web (FSE'23) |
| 5 | Nebula | https://github.com/berylliumsec/nebula | https://codewiki.google/github.com/berylliumsec/nebula | https://deepwiki.com/berylliumsec/nebula | 2023-09-30 | Asistente CLI de pentesting con soporte de LLM local |
| 6 | nyuctf_agents (D-CIPHER) | https://github.com/NYU-LLM-CTF/nyuctf_agents | https://codewiki.google/github.com/nyu-llm-ctf/nyuctf_agents | https://deepwiki.com/NYU-LLM-CTF/nyuctf_agents | 2024-03-13 | arXiv 2502.10931 |
| 7 | Pentest-Swarm-AI | https://github.com/Armur-Ai/Pentest-Swarm-AI | https://codewiki.google/github.com/armur-ai/pentest-swarm-ai | https://deepwiki.com/Armur-Ai/Pentest-Swarm-AI | 2024-03-26 | Multi-agente por enjambre con coordinación stigmergic (Go) |
| 8 | ReaperAI | https://github.com/tac01337/ReaperAI | https://codewiki.google/github.com/tac01337/reaperai | https://deepwiki.com/tac01337/ReaperAI | 2024-04-19 | arXiv 2406.07561 |
| 9 | BreachSeek (solo arXiv) | https://arxiv.org/abs/2409.03789 | — | — | 2024-08-31 | Sin repo asociado |
| 10 | vulnhuntr | https://github.com/protectai/vulnhuntr | https://codewiki.google/github.com/protectai/vulnhuntr | https://deepwiki.com/protectai/vulnhuntr | 2024-10-15 | Descubrimiento zero-shot de vulnerabilidades en Python; 0-day RCE en Ragflow |
| 11 | HackSynth | https://github.com/aielte-research/HackSynth | https://codewiki.google/github.com/aielte-research/hacksynth | https://deepwiki.com/aielte-research/HackSynth | 2024-11-27 | Arquitectura planner-summarizer; AGPL-3.0 |
| 12 | PentAGI | https://github.com/vxcontrol/pentagi | https://codewiki.google/github.com/vxcontrol/pentagi | https://deepwiki.com/vxcontrol/pentagi | 2025-01-06 | Framework multi-agente totalmente autónomo con sandboxing Docker |
| 13 | VulnBot | https://github.com/KHenryAegis/VulnBot | https://codewiki.google/github.com/khenryaegis/vulnbot | https://deepwiki.com/KHenryAegis/VulnBot | 2025-01-20 | Framework de pentesting colaborativo multi-agente con soporte RAG |
| 14 | BoxPwnr | https://github.com/0ca/BoxPwnr | https://codewiki.google/github.com/0ca/boxpwnr | https://deepwiki.com/0ca/BoxPwnr | 2025-01-26 | |
| 15 | Agentic Radar | https://github.com/splx-ai/agentic-radar | https://codewiki.google/github.com/splx-ai/agentic-radar | https://deepwiki.com/splx-ai/agentic-radar | 2025-02-12 | Escáner CLI de seguridad para workflows agénticos |
| 16 | D-CIPHER (paper) | https://arxiv.org/abs/2502.10931 | https://codewiki.google/github.com/nyu-llm-ctf/nyuctf_agents | https://deepwiki.com/NYU-LLM-CTF/nyuctf_agents | 2025-02-15 | Repo: NYU-LLM-CTF/nyuctf_agents |
| 17 | Claude Code | https://github.com/anthropics/claude-code | https://codewiki.google/github.com/anthropics/claude-code | https://deepwiki.com/anthropics/claude-code | 2025-02-22 | |
| 18 | CAI (Cybersecurity AI) | https://github.com/aliasrobotics/cai | https://codewiki.google/github.com/aliasrobotics/cai | https://deepwiki.com/aliasrobotics/cai | 2025-03-31 | Framework modular con 300+ modelos LLM; MIT investigación / licencia comercial producción |
| 19 | agent-scan (Snyk) | https://github.com/snyk/agent-scan | https://codewiki.google/github.com/snyk/agent-scan | https://deepwiki.com/snyk/agent-scan | 2025-04-07 | |
| 20 | pentestagent | https://github.com/GH05TCREW/pentestagent | https://codewiki.google/github.com/gh05tcrew/pentestagent | https://deepwiki.com/GH05TCREW/pentestagent | 2025-05-15 | Framework de pentest black-box con MCP y sesiones persistentes |
| 21 | Cyber-AutoAgent | https://github.com/westonbrown/Cyber-AutoAgent (archivado) / activo: https://github.com/double16/cyber-autoagent-ng | https://codewiki.google/github.com/westonbrown/cyber-autoagent | https://deepwiki.com/westonbrown/Cyber-AutoAgent | 2025-05-26 | 85% en el top open source de xbow |
| 22 | Decepticon | https://github.com/purpleailab/decepticon | https://codewiki.google/github.com/purpleailab/decepticon | https://deepwiki.com/purpleailab/decepticon | 2025-06-06 | |
| 23 | raink | https://github.com/BishopFox/raink | https://codewiki.google/github.com/bishopfox/raink | https://deepwiki.com/BishopFox/raink | 2025-06-12 | Ranking de documentos LLM usado en identificación de vulnerabilidades |
| 24 | ghostcrew | https://github.com/shakenetwork/ghostcrew | https://codewiki.google/github.com/shakenetwork/ghostcrew | https://deepwiki.com/shakenetwork/ghostcrew | 2025-06-13 | |
| 25 | ARTEMIS | https://github.com/Stanford-Trinity/ARTEMIS | https://codewiki.google/github.com/stanford-trinity/artemis | https://deepwiki.com/Stanford-Trinity/ARTEMIS | 2025-07-07 | |
| 26 | metis | https://github.com/arm/metis | https://codewiki.google/github.com/arm/metis | https://deepwiki.com/arm/metis | 2025-07-07 | |
| 27 | hexstrike-ai | https://github.com/0x4m4/hexstrike-ai | https://codewiki.google/github.com/0x4m4/hexstrike-ai | https://deepwiki.com/0x4m4/hexstrike-ai | 2025-07-10 | Servidor MCP con 150+ herramientas de seguridad (MIT) |
| 28 | fraim | https://github.com/fraim-dev/fraim | https://codewiki.google/github.com/fraim-dev/fraim | https://deepwiki.com/fraim-dev/fraim | 2025-07-10 | Framework para workflows de seguridad impulsados por IA (SAST/IaC) |
| 29 | RepoAudit | https://github.com/PurCL/RepoAudit | https://codewiki.google/github.com/purcl/repoaudit | https://deepwiki.com/PurCL/RepoAudit | 2025-07-10 | Agente LLM autónomo para auditoría de código a nivel de repo |
| 30 | Repeater Strike | https://github.com/hackvertor/repeat-strike | https://codewiki.google/github.com/hackvertor/repeat-strike | https://deepwiki.com/hackvertor/repeat-strike | 2025-07-17 | Extensión Burp con IA para expandir hallazgos manuales de Repeater |
| 31 | deadend-cli | https://github.com/xoxruns/deadend-cli | https://codewiki.google/github.com/xoxruns/deadend-cli | https://deepwiki.com/xoxruns/deadend-cli | 2025-07-22 | |
| 32 | Strix | https://github.com/usestrix/strix | https://codewiki.google/github.com/usestrix/strix | https://deepwiki.com/usestrix/strix | 2025-08-05 | "AI hackers" autónomos que ejecutan código y validan vulnerabilidades con PoCs (Apache-2.0) |
| 33 | hackerai | https://github.com/hackerai-tech/hackerai | https://codewiki.google/github.com/hackerai-tech/hackerai | https://deepwiki.com/hackerai-tech/hackerai | 2025-08-09 | |
| 34 | NeuroSploit | https://github.com/CyberSecurityUP/NeuroSploit | https://codewiki.google/github.com/cybersecurityup/neurosploit | https://deepwiki.com/CyberSecurityUP/NeuroSploit | 2025-08-17 | |
| 35 | BruteForceAI | https://github.com/MorDavid/BruteForceai | https://codewiki.google/github.com/mordavid/bruteforceai | https://deepwiki.com/MorDavid/BruteForceai | 2025-08-25 | Fuerza bruta con razonamiento IA y ataques automatizados de login |
| 36 | MAPTA | https://github.com/arthurgervais/mapta | https://codewiki.google/github.com/arthurgervais/mapta | https://deepwiki.com/arthurgervais/mapta | 2025-08-28 | arXiv 2508.20816 |
| 37 | Beelzebub | https://github.com/mariocandela/beelzebub | https://codewiki.google/github.com/mariocandela/beelzebub | https://deepwiki.com/mariocandela/beelzebub | 2025-08 | Toolkit ofensivo de seguridad IA y framework de honeypot |
| 38 | Hound | https://github.com/scabench-org/hound | https://codewiki.google/github.com/scabench-org/hound | https://deepwiki.com/scabench-org/hound | 2025-08 | Agentes autónomos open-source para auditoría de seguridad de código |
| 39 | agentic-soc-platform | https://github.com/FunnyWolf/agentic-soc-platform | https://codewiki.google/github.com/funnywolf/agentic-soc-platform | https://deepwiki.com/FunnyWolf/agentic-soc-platform | 2025-09-07 | |
| 40 | seclab-taskflow-agent | https://github.com/GitHubSecurityLab/seclab-taskflow-agent | https://codewiki.google/github.com/githubsecuritylab/seclab-taskflow-agent | https://deepwiki.com/GitHubSecurityLab/seclab-taskflow-agent | 2025-09-08 | GitHub Security Lab |
| 41 | auto-exploits | https://github.com/Valmarelox/auto-exploits | https://codewiki.google/github.com/valmarelox/auto-exploits | https://deepwiki.com/Valmarelox/auto-exploits | 2025-09-11 | |
| 42 | Shannon | https://github.com/KeygraphHQ/shannon | https://codewiki.google/github.com/keygraphhq/shannon | https://deepwiki.com/KeygraphHQ/shannon | 2025-09-27 | Pentester IA white-box autónomo con fuertes resultados en benchmark XBOW; el propio README de origen advierte que su comparación white-box contra un benchmark black-box no es metodológicamente correcta |
| 43 | apex | https://github.com/pensarai/apex | https://codewiki.google/github.com/pensarai/apex | https://deepwiki.com/pensarai/apex | 2025-10-10 | |
| 44 | deep-eye | https://github.com/zakirkun/deep-eye | https://codewiki.google/github.com/zakirkun/deep-eye | https://deepwiki.com/zakirkun/deep-eye | 2025-10-15 | Escáner de pentesting asistido por IA con 45+ chequeos de vulnerabilidad |
| 45 | Raptor | https://github.com/gadievron/raptor | https://codewiki.google/github.com/gadievron/raptor | https://deepwiki.com/gadievron/raptor | 2025-10-17 | |
| 46 | aracne | https://github.com/stratosphereips/aracne | https://codewiki.google/github.com/stratosphereips/aracne | https://deepwiki.com/stratosphereips/aracne | 2025-10 | Agente autónomo para operaciones SSH ofensivas y defensivas |
| 47 | CyberStrikeAI | https://github.com/Ed1s0nZ/CyberStrikeAI | https://codewiki.google/github.com/ed1s0nz/cyberstrikeai | https://deepwiki.com/Ed1s0nZ/CyberStrikeAI | 2025-11-08 | |
| 48 | medusa | https://github.com/Pantheon-Security/medusa | https://codewiki.google/github.com/pantheon-security/medusa | https://deepwiki.com/Pantheon-Security/medusa | 2025-11-15 | AGPL-3.0 |
| 49 | crossbow-agent | https://github.com/harishsg993010/crossbow-agent | https://codewiki.google/github.com/harishsg993010/crossbow-agent | https://deepwiki.com/harishsg993010/crossbow-agent | 2025-11-18 | |
| 50 | Wazuh-MCP-Server | https://github.com/gensecaihq/Wazuh-MCP-Server | https://codewiki.google/github.com/gensecaihq/wazuh-mcp-server | https://deepwiki.com/gensecaihq/Wazuh-MCP-Server | 2025-11 | Servidor MCP que expone telemetría SIEM/EDR |
| 51 | Inferno | https://github.com/Adem035/Inferno | https://codewiki.google/github.com/adem035/inferno | https://deepwiki.com/Adem035/Inferno | 2025-12-02 | |
| 52 | Syd | https://github.com/Sydsec/syd | https://codewiki.google/github.com/sydsec/syd | https://deepwiki.com/Sydsec/syd | 2025-12-03 | |
| 53 | ai-soc-agent | https://github.com/M507/ai-soc-agent | https://codewiki.google/github.com/m507/ai-soc-agent | https://deepwiki.com/M507/ai-soc-agent | 2025-12-05 | |
| 54 | AgenticRed | https://github.com/yuanjiayiy/AgenticRed | https://codewiki.google/github.com/yuanjiayiy/agenticred | https://deepwiki.com/yuanjiayiy/AgenticRed | 2025-12-11 | |
| 55 | EVA | https://github.com/ARCANGEL0/EVA | https://codewiki.google/github.com/arcangel0/eva | https://deepwiki.com/ARCANGEL0/EVA | 2025-12-15 | |
| 56 | Vulnhalla | https://github.com/cyberark/Vulnhalla | https://codewiki.google/github.com/cyberark/vulnhalla | https://deepwiki.com/cyberark/Vulnhalla | 2025-12-18 | Triage de CodeQL asistido por LLM |
| 57 | guardian-cli | https://github.com/zakirkun/guardian-cli | https://codewiki.google/github.com/zakirkun/guardian-cli | https://deepwiki.com/zakirkun/guardian-cli | 2025-12-22 | |
| 58 | VulnLLM-R | https://github.com/ucsb-mlsec/VulnLLM-R | https://codewiki.google/github.com/ucsb-mlsec/vulnllm-r | https://deepwiki.com/ucsb-mlsec/VulnLLM-R | 2025-12 | Pipeline LLM+agente enfocado en razonamiento para descubrimiento de vulnerabilidades a nivel de proyecto |
| 59 | ai-sast | https://github.com/rivian/ai-sast | https://codewiki.google/github.com/rivian/ai-sast | https://deepwiki.com/rivian/ai-sast | 2026-01-20 | |
| 60 | burp-ai-agent | https://github.com/six2dez/burp-ai-agent | https://codewiki.google/github.com/six2dez/burp-ai-agent | https://deepwiki.com/six2dez/burp-ai-agent | 2026-01-27 | Integra con Burp Suite |
| 61 | praxis | https://github.com/originsec/praxis | https://codewiki.google/github.com/originsec/praxis | https://deepwiki.com/originsec/praxis | 2026-01-27 | |
| 62 | arXiv 2602.02164 | https://arxiv.org/html/2602.02164v2 | — | — | ~2026-02-01 | Paper de febrero 2026, sin código público |
| 63 | llmitm | https://github.com/cybersharkvin/llmitm | https://codewiki.google/github.com/cybersharkvin/llmitm | https://deepwiki.com/cybersharkvin/llmitm | 2026-02-04 | |
| 64 | redamon | https://github.com/samugit83/redamon | https://codewiki.google/github.com/samugit83/redamon | https://deepwiki.com/samugit83/redamon | 2026-02-08 | |
| 65 | CyberStrike | https://github.com/CyberStrikeus/CyberStrike | https://codewiki.google/github.com/cyberstrikeus/cyberstrike | https://deepwiki.com/CyberStrikeus/CyberStrike | 2026-02-14 | |
| 66 | grimoire | https://github.com/JoranHonig/grimoire | https://codewiki.google/github.com/joranhonig/grimoire | https://deepwiki.com/JoranHonig/grimoire | 2026-02-16 | |
| 67 | ironcurtain | https://github.com/provos/ironcurtain | https://codewiki.google/github.com/provos/ironcurtain | https://deepwiki.com/provos/ironcurtain | 2026-02-21 | |
| 68 | OpenAnt | https://github.com/knostic/OpenAnt | https://codewiki.google/github.com/knostic/openant | https://deepwiki.com/knostic/OpenAnt | 2026-02-26 | |
| 69 | airecon | https://github.com/pikpikcu/airecon | https://codewiki.google/github.com/pikpikcu/airecon | https://deepwiki.com/pikpikcu/airecon | 2026-03-05 | |
| 70 | agentflow | https://github.com/berabuddies/agentflow | https://codewiki.google/github.com/berabuddies/agentflow | https://deepwiki.com/berabuddies/agentflow | 2026-03-08 | |
| 71 | ai-web3-security | https://github.com/pashov/ai-web3-security | https://codewiki.google/github.com/pashov/ai-web3-security | https://deepwiki.com/pashov/ai-web3-security | 2026-03-12 | |
| 72 | llmchainhunter | https://github.com/atredispartners/llmchainhunter | https://codewiki.google/github.com/atredispartners/llmchainhunter | https://deepwiki.com/atredispartners/llmchainhunter | 2026-03-16 | Diseño/runbook Claude Code para búsqueda de cadenas de gadget de deserialización Java |
| 73 | operant-mcp | https://github.com/operantlabs/operant-mcp | https://codewiki.google/github.com/operantlabs/operant-mcp | https://deepwiki.com/operantlabs/operant-mcp | 2026-03-22 | Servidor MCP con 51 herramientas de testing en 19 módulos (SQLi, XSS, CMDi, SSRF, path traversal, forense PCAP, recon, forense de memoria, análisis de malware). Instalar vía `npx operant-mcp` |
| 74 | ctf-agent | https://github.com/verialabs/ctf-agent | https://codewiki.google/github.com/verialabs/ctf-agent | https://deepwiki.com/verialabs/ctf-agent | 2026-03-23 | |
| 75 | red-run | https://github.com/blacklanternsecurity/red-run | https://codewiki.google/github.com/blacklanternsecurity/red-run | https://deepwiki.com/blacklanternsecurity/red-run | 2026-03-30 | Toolkit de evaluación de seguridad para Claude Code |
| 76 | xalgorix | https://github.com/xalgord/xalgorix | https://codewiki.google/github.com/xalgord/xalgorix | https://deepwiki.com/xalgord/xalgorix | 2026-03 | Agente de pentesting IA open-source |
| 77 | VulnVibes | https://github.com/anshumanbh/vulnvibes | https://codewiki.google/github.com/anshumanbh/vulnvibes | https://deepwiki.com/anshumanbh/vulnvibes | 2026-04-02 | Agente IA que razona entre microservicios para hallar vulnerabilidades reales |
| 78 | DeepZero | https://github.com/416rehman/DeepZero | https://codewiki.google/github.com/416rehman/deepzero | https://deepwiki.com/416rehman/DeepZero | 2026-04-07 | |
| 79 | nano-analyzer | https://github.com/weareaisle/nano-analyzer | https://codewiki.google/github.com/weareaisle/nano-analyzer | https://deepwiki.com/weareaisle/nano-analyzer | 2026-04-14 | |
| 80 | clearwing | https://github.com/Lazarus-AI/clearwing | https://codewiki.google/github.com/lazarus-ai/clearwing | https://deepwiki.com/Lazarus-AI/clearwing | 2026-04-14 | |
| 81 | redai | https://github.com/kpolley/redai | https://codewiki.google/github.com/kpolley/redai | https://deepwiki.com/kpolley/redai | 2026-04-30 | Workbench de terminal para descubrimiento de vulnerabilidades impulsado por IA |
| 82 | deepsec | https://github.com/vercel-labs/deepsec | https://codewiki.google/github.com/vercel-labs/deepsec | https://deepwiki.com/vercel-labs/deepsec | 2026-04 | Harness de descubrimiento de vulnerabilidades con agente de codificación |
| 83 | pentest-ai | https://github.com/0xSteph/pentest-ai | https://codewiki.google/github.com/0xsteph/pentest-ai | https://deepwiki.com/0xSteph/pentest-ai | 2026-04 | Servidor MCP de seguridad ofensiva con herramientas envueltas y agentes especialistas |
| 84 | vlnr | https://github.com/nandrzej/vlnr | https://codewiki.google/github.com/nandrzej/vlnr | https://deepwiki.com/nandrzej/vlnr | 2026-04 | Agente de seguridad IA para revisión de supply-chain Python, generación de exploits y validación Docker |
| 85 | claude-mythos | https://github.com/anshug/claude-mythos | https://codewiki.google/github.com/anshug/claude-mythos | https://deepwiki.com/anshug/claude-mythos | 2026-04 | Framework de descubrimiento de vulnerabilidades orientado a Claude |
| 86 | AIMap | https://github.com/BishopFox/aimap | https://codewiki.google/github.com/bishopfox/aimap | https://deepwiki.com/BishopFox/aimap | 2026-05-07 | Descubre, fingerprints, puntúa y testea infraestructura de agentes de IA expuesta a internet |
| 87 | RAMPART | https://github.com/microsoft/RAMPART | https://codewiki.google/github.com/microsoft/rampart | https://deepwiki.com/microsoft/RAMPART | 2026-05-28 | Framework pytest-native para safety/seguridad de apps agénticas |
| 88 | autopentest-ai | https://github.com/bhavsec/autopentest-ai | https://codewiki.google/github.com/bhavsec/autopentest-ai | https://deepwiki.com/bhavsec/autopentest-ai | — | |

### 3.2 Otros Agentes y Frameworks de Pentest / Red Team (no listados en la tabla anterior)

- **PentestGPT (versión hackerai-tech)** — asistencia avanzada para escanear, explotar y analizar aplicaciones web, redes y entornos cloud. https://github.com/hackerai-tech/PentestGPT
- **DeepExploit** — framework de pentesting totalmente automatizado usando machine learning; refuerza sus estrategias de ataque con RL. https://github.com/13o-bbr-bbq/machine_learning_security
- **Continuous CyberBattleSim** — simulación para entrenar agentes de RL escalables en descubrimiento de rutas de ataque críticas en redes. https://github.com/terranovafr/C-CyberBattleSim (paper: https://ieeexplore.ieee.org/document/11352493)
- **CAI – Cybersecurity AI** — framework modular listo para bug-bounty con 300+ modelos LLM soportados; MIT para investigación, licencia comercial separada para producción/on-prem. (Alias Robotics) https://github.com/aliasrobotics/cai
- **HexStrike-AI** — servidor MCP que expone 150+ herramientas de seguridad (nmap, gobuster, nuclei…) a agentes de IA (MIT). https://github.com/0x4m4/hexstrike-ai
- **Deep Eye** — escáner de pentesting asistido por IA que orquesta múltiples proveedores LLM para generación de payloads, 45+ chequeos de vulnerabilidad, testing asistido por CVE/RAG, triage de IA. MIT; solo uso autorizado. https://github.com/zakirkun/deep-eye
- **pentest-ai / pentest-ai-agents** — servidor MCP de seguridad ofensiva con 200+ herramientas envueltas y colección de subagentes Claude Code para investigación de pentesting autorizada. https://github.com/0xSteph/pentest-ai · https://github.com/0xSteph/pentest-ai-agents
- **DarkMoon** ⚠️ — plataforma de pentesting autónomo con IA que orquesta agentes especializados de web, AD, Kubernetes, CMS y frameworks a través de un toolbox Docker controlado por MCP, con tokenización de privacidad local. Licencia GPL-3.0. (ASCIT31) https://github.com/ASCIT31/Dark-Moon
- **xOffense** — framework de pentesting multi-agente con LLMs mejorados con conocimiento ofensivo. https://arxiv.org/abs/2509.13021
- **Penligent** — "el primer agentic AI hacker del mundo"; interfaz de lenguaje natural, red-teaming autónomo. https://penligent.ai/
- **HALO** — agente de pentesting autónomo completamente local, potenciado por un modelo Gemma 4-12B local y servidor MCP Flask; bucle recon→ataque→reporte, sin necesidad de API keys. https://github.com/XenoCoreGiger31/GEMMA-by-GOOGLE
- **T3MP3ST** ⚠️ — meta-harness de seguridad ofensiva autónomo que envuelve agentes de codificación locales o basados en API en un workflow multi-agente de recon-a-exploit, con MCP/API y UI de War Room. AGPL-3.0. https://github.com/elder-plinius/T3MP3ST
- **AIDA** ⚠️ — agente de pentesting autónomo agnóstico de modelo ejecutándose dentro de un entorno Docker aislado. AGPL-3.0. https://github.com/Vasco0x4/AIDA
- **cyber-security-llm-agents** ⚠️ — agentes basados en AutoGen para tareas de ciberseguridad (presentado en RSAC 2024). (NVISO) https://github.com/NVISOsecurity/cyber-security-llm-agents
- **hackGPT** ⚠️ — toolkit de seguridad ofensiva basado en LLM. https://github.com/NoDataFound/hackGPT
- **ShiftGrid** — motor de prompts que convierte a Claude Code en un pentester transparente human-in-the-loop, estructurando engagements mediante checklists y notas expuestas vía API. https://github.com/BuFuuu/shiftgrid
- **BugTraceAI** ⚠️ — escáner autónomo de seguridad de aplicaciones web self-hosted que combina reconocimiento, agentes de exploit especialistas, fuzzers en Go y validación Playwright. AGPL-3.0, beta. https://github.com/BugTraceAI/BugTraceAI-CLI · https://github.com/BugTraceAI/BugTraceAI · https://github.com/BugTraceAI/BugTraceAI-WEB · https://github.com/BugTraceAI/BugTraceAI-Launcher
- **HunterX** — motor de seguridad ofensiva asistido por IA que orquesta reconocimiento, coordinación de herramientas de seguridad, detección y validación de vulnerabilidades, y hallazgos listos para reportar. (NullC0d3) https://github.com/nullc0d30/HunterX
- **agentic_security** — escáner de vulnerabilidades de LLM especializado en sistemas y workflows agénticos. https://github.com/msoedov/agentic_security
- **Zen-AI-Pentest** — framework multi-agente usando agentes autónomos + utilidades de seguridad. *(sin URL confirmada en el material original)*
- **AI-OPS** — asistente para desarrollo de exploits e investigación. https://github.com/antoninoLorenzo/AI-OPS
- **BurpGPT** — extensión de Burp Suite integrando LLMs para escaneo pasivo. https://github.com/aress31/burpgpt · https://burpgpt.app
- **Cynative** — CLI de investigación de seguridad IA local que ejecuta código en un sandbox integrado para investigar AWS, GCP, Azure, Kubernetes, GitHub y GitLab; read-only por defecto. https://github.com/cynative/cynative

### 3.3 DARPA AI Cyber Challenge (AIxCC)

- **AIxCC Open Source Archive** — sistemas, artefactos y recursos de la competencia liberados para estudio e investigación defensiva. https://archive.aicyberchallenge.com/
- **DARPA 2025 AIxCC results announcement** — anuncio oficial de resultados. https://www.darpa.mil/news/2025/aixcc-results

| # | Equipo | CRS | Lugar | Sitio del equipo | Repositorios | Docs/writeups |
|---|---|---|---|---|---|---|
| 1 | Team Atlanta | ATLANTIS | 1º | https://team-atlanta.github.io/ | Semi-finales: https://github.com/Team-Atlanta/aixcc-asc-atlantis · Finales: https://github.com/Team-Atlanta/aixcc-afc-atlantis | Blog: https://team-atlanta.github.io/blog/post-afc/ · Paper arXiv: https://arxiv.org/abs/2509.14589 · PDF: https://daeryong.me/team-atlanta-atlantis.pdf |
| 2 | Trail of Bits | Buttercup | 2º | https://trailofbits.com/buttercup/ | Semi-finales: https://github.com/trailofbits/asc-buttercup · Finales: https://github.com/trailofbits/afc-buttercup | Overview: https://trailofbits.com/buttercup/ · Slides DEF CON: https://www.trailofbits.com/documents/DEFCON_AIxCC_Stage_Talk.pdf |
| 3 | Theori | RoboDuck | 3º | https://theori.io/ | Semi-finales: https://github.com/theori-io/aixcc-asc-archive · Finales: https://github.com/theori-io/aixcc-afc-archive · Públicos: https://github.com/theori-io/aixcc-public | Blog: https://theori.io/blog/aixcc-and-roboduck-63447 |
| 4 | All You Need Is A Fuzzing Brain | FuzzingBrain | 4º | https://all-you-need-is-a-fuzzing-brain.github.io/ | Semi-finales: https://github.com/o2lab/asc-crs-all-you-need-is-a-fuzzing-brain · Finales: https://github.com/o2lab/afc-crs-all-you-need-is-a-fuzzing-brain | Paper: https://arxiv.org/abs/2509.07225 · PDF: https://www.doc.ic.ac.uk/~afd/papers/2025/AIxCC.pdf |
| 5 | Shellphish | ARTIPHISHELL | 5º | https://shellphish.net/aixcc/ | Repo principal: https://github.com/shellphish/artiphishell · Tag semi-finales: https://github.com/shellphish/artiphishell/releases/tag/Semi-Finals · Tag finales: https://github.com/shellphish/artiphishell/releases/tag/Finals | Postmortem: https://support.shellphish.net/blog/2025/08/22/shellphish-x-aixcc-pm/ |
| 6 | 42-b3yond-6ug | BugBuster | 6º | https://b3yond.org/ (CRS: https://b3yond.org/crs) | Semi-finales: https://github.com/42-b3yond-6ug/42-b3yond-6ug-asc · Finales: https://github.com/42-b3yond-6ug/42-b3yond-6ug-crs | Retrospectivas: https://b3yond.org/crs |
| 7 | Lacrosse (SIFT) | Lacrosse CRS | 7º | https://www.sift.net/ | Semi-finales: https://github.com/siftech/asc-crs-lacrosse · Finales: https://github.com/siftech/afc-crs-lacrosse | CTF Radiooo: https://ctfradi.ooo/2025/07/17/01C-lacrosses-aixcc-final-submission.html · Playlist entrevistas: https://www.youtube.com/playlist?list=PLFVmyX_rOm09ULieQIiA3Px2asBBNQVC5 |

### 3.4 Tencent Cybersecurity AI Challenge (otoño 2025)

Competencia de Tencent: https://zc.tencent.com/competition/competitionHackathon?code=cha004

| # | Nombre | GitHub | CodeWiki | DeepWiki |
|---|---|---|---|---|
| 1 | ctfSolver | https://github.com/passer-W/ctfSolver | https://codewiki.google/github.com/passer-w/ctfsolver | https://deepwiki.com/passer-W/ctfSolver |
| 2 | LuaN1aoAgent | https://github.com/SanMuzZzZz/LuaN1aoAgent | https://codewiki.google/github.com/sanmuzzzzz/luan1aoagent | https://deepwiki.com/SanMuzZzZz/LuaN1aoAgent |
| 3 | tinyctfer | https://github.com/chainreactors/tinyctfer | https://codewiki.google/github.com/chainreactors/tinyctfer | https://deepwiki.com/chainreactors/tinyctfer |
| 4 | hackthon_demo | https://github.com/Ghr07h/hackthon_demo | https://codewiki.google/github.com/ghr07h/hackthon_demo | https://deepwiki.com/Ghr07h/hackthon_demo |
| 5 | Neuro-Sploit | https://github.com/Neuro-Sploit | — | — (enlace de org/usuario, no repo) |
| 6 | xbow-competition | https://github.com/m-sec-org/xbow-competition | https://codewiki.google/github.com/m-sec-org/xbow-competition | https://deepwiki.com/m-sec-org/xbow-competition |
| 7 | Cruiser_public | https://github.com/TJR181/Cruiser_public | https://codewiki.google/github.com/tjr181/cruiser_public | https://deepwiki.com/TJR181/Cruiser_public |
| 8 | CHYing-agent | https://github.com/yhy0/CHYing-agent | https://codewiki.google/github.com/yhy0/chying-agent | https://deepwiki.com/yhy0/CHYing-agent |
| 9 | SickHackShark | https://github.com/SickHackPark/SickHackShark | https://codewiki.google/github.com/sickhackpark/sickhackshark | https://deepwiki.com/SickHackPark/SickHackShark |
| 10 | PenAgent | https://github.com/lcz24/PenAgent | https://codewiki.google/github.com/lcz24/penagent | https://deepwiki.com/lcz24/PenAgent |
| 11 | newmapta | https://github.com/HUST-JYHLab/newmapta | https://codewiki.google/github.com/hust-jyhlab/newmapta | https://deepwiki.com/HUST-JYHLab/newmapta |
| 12 | sub-agent-autopt | https://github.com/yyy1mu/sub-agent-autopt | https://codewiki.google/github.com/yyy1mu/sub-agent-autopt | https://deepwiki.com/yyy1mu/sub-agent-autopt |
| 13 | H-Pentest | https://github.com/hexian2001/H-Pentest | https://codewiki.google/github.com/hexian2001/h-pentest | https://deepwiki.com/hexian2001/H-Pentest |
| 14 | AgentNote | https://github.com/C1JC/AgentNote | https://codewiki.google/github.com/c1jc/agentnote | https://deepwiki.com/C1JC/AgentNote |
| 15 | BUUCTF_Agent | https://github.com/MuWinds/BUUCTF_Agent | https://codewiki.google/github.com/muwinds/buuctf_agent | https://deepwiki.com/MuWinds/BUUCTF_Agent |

### 3.5 Soluciones Empresariales / Closed Source

- Aikido — https://www.aikido.dev/attack/aipentest
- AISLE — https://aisle.com/
- bugbunny ai — https://bugbunny.ai/
- Google Project Zero / DeepMind — Project Naptime → Big Sleep — https://projectzero.googleblog.com/2024/06/project-naptime.html · https://projectzero.googleblog.com/2024/10/from-naptime-to-big-sleep.html
- CalypsoAI — https://calypsoai.com/
- Casco — https://casco.com/
- Corridor dev — https://corridor.dev/
- Dreadnode — https://dreadnode.io/
- Hacktron — https://www.hacktron.ai/
- Harmony Intelligence — https://www.harmonyintelligence.com/
- Hex Security — https://hex.co/
- Horizon3.ai — https://horizon3.ai/
- Hound (comercial) — https://cyberhound.ai/
- KinoSec — https://kinosec.ai/
- MindFort — https://mindfort.ai/
- Mindgard — https://mindgard.ai/
- Novee — https://novee.security/
- Origin / Prelude — https://www.originhq.com/ · https://www.preludesecurity.com/
- Penligent — https://penligent.ai/
- Pensar — https://www.pensarai.app/
- Pentera — https://pentera.io/
- PentX — https://pentx.ai/
- qriousec — https://qriousec.github.io/
- Revelion ai — https://www.revelion.ai/
- RunSybil — https://www.runsybil.com
- Shinobi Security — https://shinobi.security
- SPLX — https://splx.ai/
- Terra Security — https://www.terra.security
- Theori — Xint / Xint Code — https://xint.io/ · https://code.xint.io/ · https://theori.io/
- Veria Labs — https://verialabs.com/
- XBOW — https://xbow.com

### 3.6 CTF, Exploit y Bug-Bounty (Agentes y Benchmarks)

- **SWE-agent (EnIGMA)** 🟢🔬 — modo ofensivo-CTF EnIGMA; estado del arte en NYU CTF, InterCode-CTF y Cybench (rama v0.7). https://github.com/SWE-agent/SWE-agent
- **Cybench** 🔬 — 40 tareas de CTF profesional en 4 competencias; ampliamente usado por institutos de seguridad de IA. *(sin URL propia confirmada — repo `andyzorigin/cybench` habitual, no verificado en la fuente)*
- **NYU CTF Bench** 🔬 — desafíos CTF de CSAW Dockerizados para evaluación controlada de agentes LLM. https://github.com/NYU-LLM-CTF/NYU_CTF_Bench
- **CTFTiny** 🔬⚠️ — benchmark CTF liviano del grupo NYU LLM CTF; licencia GPL-2.0. *(sin URL propia confirmada en la fuente original)*
- **InterCode** 🔬 — benchmark de codificación interactiva incl. InterCode-CTF. *(sin URL propia confirmada en la fuente original)*
- **inspect_evals** 🟢🔬 — suite de evaluación mantenida de Inspect AI con múltiples benchmarks y tareas de ciberseguridad. (UK AI Security Institute) *(sin URL propia confirmada en la fuente original)*
- **BountyBench** 🔬 — 25 sistemas reales / 40 bug bounties para evaluación Detect-Exploit-Patch. *(sin URL propia confirmada en la fuente original)*
- **Cyber-Zero** 🔬 — entrena agentes de ciberseguridad sin runtime; incluye un scaffold EnIGMA+. (Amazon Science) *(sin URL propia confirmada en la fuente original)*
- **ExploitBench** 🔬 — mide el progreso de agentes de IA en escaleras de exploit de V8/Chromium. *(sin URL propia confirmada en la fuente original)*
- **AI Goat** 🟢🔬⚠️ — CTF LLM local vulnerable-by-design para aprender prompt injection, manejo inseguro de output, fuga de datos y agencia excesiva. Licencia GPL-2.0. https://github.com/dhammon/ai-goat
- **AIGoat** 🟢🔬⚠️ — playground de seguridad LLM local-first vulnerable con labs guiados de ataque OWASP LLM Top 10, retos CTF y target de shopping asistente respaldado por Ollama. Código de plataforma Apache-2.0; contenido de entrenamiento CC BY-NC-SA-4.0. *(sin URL propia confirmada en la fuente original)*
- **LLMVault** 🟢🔬 — plataforma de entrenamiento en seguridad LLM intencionalmente vulnerable con labs OWASP LLM Top 10, retos estilo CTF, hints, scoring y guía de mitigación. *(sin URL propia confirmada en la fuente original)*
- **Damn Vulnerable LLM Agent** 🟢🔬 — agente ReAct de LangChain deliberadamente vulnerable para practicar prompt-injection y ataques de inyección Thought/Action/Observation. (ReversecLabs/WithSecure) https://github.com/ReversecLabs/damn-vulnerable-llm-agent
- **DamnVulnerableLLMProject** — app LLM deliberadamente vulnerable para entrenamiento/educación. (harishsg993010) https://github.com/harishsg993010/DamnVulnerableLLMProject
- **LLM Security CTF** — CTFs de LLM vulnerables gratuitos basados en web. (TrustAI-laboratory) https://github.com/TrustAI-laboratory/LLM-Security-CTF
- **AI Goat (Orca Security)** 🟢🔬 — lab de AWS y Terraform deliberadamente vulnerable para aprender riesgos de infraestructura IA/ML (compromiso de supply-chain de modelos, envenenamiento de datos). (Orca Security Research) *(sin URL propia confirmada en la fuente original)*
- **claude-bug-bounty** 🟢 — plugin de Claude Code que orquesta recon → clases de vulnerabilidad → reporting. https://github.com/mrgick/claude-bug-bounty
- **Bug-Bounty-Agents** 🟢 — 43 personas de agente IA para Claude Code / Copilot / Cursor a lo largo del ciclo de vida de bug-bounty. *(sin URL propia confirmada en la fuente original)*
- **ai-exploits** 🟢 — exploits reales de IA/ML (módulos Metasploit + plantillas Nuclei) para MLflow, Ray, H2O. (Protect AI) https://github.com/protectai/ai-exploits
- **CyberGym** 🟢🔬 — framework de evaluación a gran escala para análisis de vulnerabilidades de agentes de IA en tareas reales, con infraestructura de desafío desplegada localmente. (UC Berkeley/Sunblaze) *(sin URL propia confirmada en la fuente original)*
- **CVE-Bench** 🟢🔬 — benchmark ICML 2025 que evalúa agentes de IA contra entornos Docker reproducibles para CVEs reales de severidad crítica en aplicaciones web. *(sin URL propia confirmada en la fuente original)*
- **SCAM** 🟢🔬 — benchmark para medir si agentes que usan herramientas reconocen y resisten estafas realistas, ingeniería social, solicitudes de credenciales, suplantación e instrucciones multi-turno inseguras. (1Password) *(sin URL propia confirmada en la fuente original)*
- **AIRTBench-Code** 🟢🔬 — harness y dataset de investigación para evaluar agentes autónomos de red-team de IA en desafíos CTF de seguridad IA/ML. (Dreadnode) *(sin URL propia confirmada en la fuente original)*
- **LivePI** 🔬⚠️ — artefacto de reproducibilidad para un benchmark de prompt-injection indirecta production-like, abarcando superficies en vivo pero controladas de email, chat, web, archivo local, repositorio y wallet. *(sin URL propia confirmada en la fuente original)*
- **Gandalf** — juego de prompt injection con niveles de dificultad (el mayor experimento de red team del mundo). (Lakera) https://gandalf.lakera.ai/
- **HackAPrompt 1.0 / 2.0** — competencia y hackathon de prompt hacking a gran escala. https://www.hackaprompt.com/
- **DEF CON AI CTF (AI Village)** — CTF anual de seguridad LLM. https://www.kaggle.com/competitions/ai-village-ctf

---

## 4. AppSec y Vulnerability Research con IA

El rol de mayor valor de la IA en AppSec es mejorar descubrimiento, triage, validación, reporting y remediación mientras las personas siguen siendo responsables de las decisiones de seguridad.

### 4.1 SAST impulsado por IA

- **Vulnhuntr** 🟢 — descubrimiento zero-shot de vulnerabilidades en repos Python vía análisis de cadena de llamadas LLM; acreditado con un RCE 0-day en Ragflow. (Protect AI) https://github.com/protectai/vulnhuntr
- **deepsec** 🟢 — harness de seguridad impulsado por agentes para escanear grandes bases de código con agentes de codificación, ejecuciones paralelas resumibles, matchers personalizados y revalidación opcional. (Vercel Labs) https://github.com/vercel-labs/deepsec
- **Codex Security** 🟠 — CLI y SDK TypeScript que usan Codex Security para encontrar, validar y ayudar a arreglar vulnerabilidades en una base de código. (OpenAI) https://github.com/openai/codex-security
- **open·kritt** 🟢⚠️ — plataforma self-hosted que orquesta Codex o Claude Code a través de workflows de investigación de vulnerabilidades enfocados, luego valida, deduplica, rankea y reporta hallazgos. (Kritt AI) https://github.com/Kritt-ai/open-kritt
- **Visa Vulnerability Agentic Harness** 🟢 — pipeline SAST agéntico para descubrimiento autónomo de vulnerabilidades, verificación de explotabilidad, reporting SARIF/Markdown, remediación y validación usando modelos de IA frontier. Apache-2.0. https://github.com/visa/visa-vulnerability-agentic-harness
- **defending-code-reference-harness** 🟢 — skills de referencia de Claude Code y pipeline autónomo de descubrimiento de vulnerabilidades para threat modeling, escaneo estático, triage, descubrimiento de bugs de memoria C/C++ verificado por ejecución, reporting y generación de parches. (Anthropic) https://github.com/anthropics/defending-code-reference-harness
- **rust-in-peace** 🟢 — fork de seguridad en Rust del harness de referencia de Anthropic, agregando un perfil Rust para revisión agéntica de bugs de memoria unsafe/FFI. (Sergey Gordeychik) https://github.com/scadastrangelove/rust-in-peace
- **claude-code-security-review** 🟠 — GitHub Action SAST semántico oficial basado en Claude que revisa diffs de PR. (Anthropic) https://github.com/anthropics/claude-code-security-review
- **IRIS** 🟢🔬 — SAST neurosimbólico que combina LLMs con CodeQL para detección de vulnerabilidades Java (MIT). https://github.com/iris-sast/iris
- **sast-skills** 🟢 — skills de agente que convierten a los asistentes de codificación de IA en un escáner SAST multi-agente. (utkusen) https://github.com/utkusen/sast-skills
- **llm-sast-scanner** 🟢 — skill SAST para agentes de codificación IA con análisis source-to-sink estructurado a través de 34 clases de vulnerabilidad. https://github.com/SunWeb3Sec/llm-sast-scanner
- **sast-ai-workflow** 🟢 — workflow LangGraph para revisar hallazgos de análisis estático, reducir falsos positivos y producir output de revisión de vulnerabilidades. (Red Hat Ecosystem AppEng) https://github.com/RHEcosystemAppEng/sast-ai-workflow
- **llm-security-scanner** 🟢⚠️ — escáner de código impulsado por LLM que abre issues de GitHub por cada hallazgo. https://github.com/iknowjason/llm-security-scanner
- **Trail of Bits Skills** 🟢⚠️ — skills de workflow de seguridad compatibles con Claude Code y Codex para revisión de código, revisión diferencial, análisis de falsos positivos, chequeos de supply-chain, auditoría de GitHub Actions y generación de reglas Semgrep. https://github.com/trailofbits/skills
- **OpenHack** 🟢 — workspace de revisión de seguridad white-box guiado por código-fuente que orquesta agentes a través de reconocimiento, búsqueda de vulnerabilidades, validación, captura de evidencia y reporting. (Hadrian Security) https://github.com/hadriansecurity/OpenHack
- **OpenHack (openhackai)** — escáner de código-fuente multi-agente y sistema de validación (proyecto distinto, mismo nombre). https://github.com/openhackai/OpenHack
- **Buttercup** 🟢🔬⚠️ — sistema de razonamiento cibernético multi-componente para encontrar, validar y parchear vulnerabilidades de software con workflows de agente coordinados. AGPL-3.0. (Trail of Bits) https://github.com/trailofbits/buttercup
- **CodeQL** — análisis de código semántico y ecosistema de queries; compañero determinístico de la revisión asistida por IA. https://github.com/github/codeql
- **OSS-Fuzz** — fuzzing continuo para proyectos open-source críticos. https://github.com/google/oss-fuzz
- **SARIF** — formato estándar para resultados de análisis estático e interoperabilidad de revisión.
- **AutoPatchBench** — benchmarking para reparación automatizada de vulnerabilidades detectadas por fuzzing. https://engineering.fb.com/2025/04/29/ai-research/autopatchbench-benchmark-ai-powered-security-fixes/
- **VLoc Bench** — benchmark agéntico en dos fases (500 tareas, 290 repos, 147 tipos CWE) evaluando localización de vulnerabilidades y verificación de parches basada en terminal. https://github.com/cisco-foundation-ai/vulnerability-localization-benchmark
- **SecLLMHolmes** — framework automatizado para evaluación sistemática de detección de vulnerabilidades LLM en múltiples dimensiones. https://github.com/ai4cloudops/SecLLMHolmes

### 4.2 Autotriage de Hallazgos de Seguridad

- **nuclei-autotriage** 🟢⚠️ — triage LLM en dos etapas (falsifier + pase de red-team) de hallazgos JSONL de Nuclei vía endpoints compatibles con OpenAI (vLLM/Ollama). EULA personal/no comercial restrictiva. (CyberOK) https://github.com/cyberok-org/nuclei-autotriage
- **seclab-taskflow-agent** 🟢 — framework de agente de taskflow dirigido por YAML para triage de alertas CodeQL/SAST y filtrado de falsos positivos. (GitHub Security Lab) https://github.com/GitHubSecurityLab/seclab-taskflow-agent
- **honeyslop** 🟢 — decoys de código-canario para triage de reportes de vulnerabilidad alucinados por IA ("slop") que inundan programas de bug-bounty. https://github.com/gadievron/honeyslop
- **nano-analyzer** 🟢🔬 — pipeline LLM mínimo de tres etapas (contexto → escaneo → triage escéptico) para descubrimiento de zero-days en C/C++. (AISLE) https://github.com/weareaisle/nano-analyzer
- **SigmaOptimizer** 🟢 — genera, testea y refina reglas Sigma a partir de logs reales con chequeo de falsos positivos. https://github.com/YusukeJustinNakajima/SigmaOptimizer
- **ai-soc-triage-assistant** 🟢⚠️ — asistente de triage de alertas SOC con guardrails de prompt-injection, validación de output y mapeo MITRE ATT&CK. https://github.com/pranavibunny/ai-soc-triage-assistant
- **Vulnhalla** 🟢⚠️ — triage de CodeQL asistido por LLM para reducir falsos positivos durante la búsqueda de vulnerabilidades. AGPL-3.0. (CyberArk) https://github.com/cyberark/Vulnhalla
- **CVE-LMTune** — framework unificado para fine-tuning, evaluación e inferencia en vivo de modelos de lenguaje para clasificación automatizada de vulnerabilidades basada en taxonomías MITRE. https://github.com/terranovafr/CVE-LMTune (paper: https://hal.science/hal-05500820)

### 4.3 Fuzzing dirigido por LLM

**Generación de harness/target:**

- **oss-fuzz-gen** 🟢 — generación de harness de fuzzing dirigida por LLM para OSS-Fuzz; reportó 26 vulnerabilidades reales (incl. CVE-2024-9143 en OpenSSL). (Google) https://github.com/google/oss-fuzz-gen
- **PromptFuzz** 🟢🔬⚠️ — prompts mutados por LLM para generar fuzz drivers de librerías C/C++ (Rust). https://github.com/PromptFuzz/PromptFuzz
- **Fuzz4All** 🟢🔬 — fuzzer LLM "universal" a través de compiladores/lenguajes (ICSE 2024). https://github.com/fuzz4all/fuzz4all
- **ChatAFL** 🟢🔬 — fuzzing de protocolos guiado por LLM extendiendo AFLNet (NDSS'24). https://github.com/ChatAFLndss/ChatAFL
- **TitanFuzz** 🟢🔬⚠️ — primer fuzzer basado en LLM para PyTorch/TensorFlow (ISSTA'23). https://github.com/ise-uiuc/TitanFuzz

**Fuzzing del propio LLM:**

- **LLMFuzzer** 🟢🔬 — primer framework open-source de fuzzing para integraciones de API LLM. https://github.com/mnns/LLMFuzzer
- **ps-fuzz** 🟠 — fuzzer de endurecimiento de system-prompt; 16 ataques × 16 proveedores. (Prompt Security) https://github.com/prompt-security/ps-fuzz
- **FuzzyAI** 🟠 — fuzzer LLM automatizado para jailbreaks/prompt injection. (CyberArk) https://github.com/cyberark/FuzzyAI

### 4.4 Threat Modeling con IA

- **tachi** 🟢 — harness de threat modeling y detección de vulnerabilidades por razonamiento de IA para Claude Code que despliega 14 agentes de amenaza especializados (6 STRIDE, 5 LLM, 3 agénticos) contra una descripción de arquitectura en Mermaid, C4, PlantUML, ASCII o texto libre. (David Matousek) https://github.com/davidmatousek/tachi
- **STRIDE GPT** 🟢 — herramienta de threat modeling impulsada por LLM que genera modelos de amenaza STRIDE, árboles de ataque, DFDs, puntajes de riesgo DREAD y casos de test Gherkin. (Matthew Adams) https://github.com/mrwadams/stride-gpt

### 4.5 Ingeniería Inversa asistida por IA

- **Gepetto** 🟢 — plugin de IDA Pro: GPT agrega comentarios y nombres de variables significativos. https://github.com/JusticeRage/Gepetto
- **ida-pro-mcp** 🟢 — puente MCP para IDA Pro que expone decompile, disassemble, xref, rename y workflows de debugging a clientes LLM. https://github.com/mrexodia/ida-pro-mcp
- **GhidraMCP** 🟢 — servidor MCP que expone operaciones de ingeniería inversa de Ghidra a cualquier LLM con capacidad MCP. https://github.com/LaurieWired/GhidraMCP
- **ReVa** 🟢 — asistente de ingeniería inversa enfocado en Ghidra con soporte MCP, integración Claude Skills y workflows de análisis extenso. https://github.com/cyberkaida/reverse-engineering-assistant
- **GhidrAssistMCP** 🟢 — extensión MCP nativa de Ghidra con amplia cobertura de herramientas, soporte headless y control de herramientas sensible a la seguridad. https://github.com/symgraph/GhidrAssistMCP
- **ghidra-mcp** 🟢 — servidor MCP de Ghidra con gran cobertura de herramientas, plugin GUI, servidor headless y carga perezosa de herramientas. https://github.com/bethington/ghidra-mcp
- **GhidrOllama** 🟢⚠️ — script de Ghidra usando la API de Ollama para análisis/renombrado de funciones. https://github.com/lr-m/GhidrOllama
- **GhidraGPT** 🟢 — plugin de Ghidra que integra LLMs para refactorización y análisis de código automatizado. https://github.com/weirdmachine64/GhidraGPT
- **LLM4Decompile** 🟢🔬⚠️ — proyecto de investigación para decompilación binario-a-C con LLMs; código MIT, pesos del modelo con licencia más restrictiva. https://github.com/albertan017/LLM4Decompile
- **x64dbg_mcp** 🟢 — servidor MCP que expone operaciones de debugging/ingeniería inversa de x64dbg a clientes IA. https://github.com/bromoket/x64dbg_mcp
- **binaryninja-mcp** 🟢 — servidor MCP para ingeniería inversa asistida por Binary Ninja. https://github.com/MCPPhalanx/binaryninja-mcp
- **OGhidra** 🟢 — análisis de Ghidra en lenguaje natural vía Ollama. (Lawrence Livermore National Lab) https://github.com/llnl/OGhidra
- **ghidra_tools (G-3PO)** 🟢 — plugin de Ghidra para análisis de código decompilado asistido por IA. (Tenable) https://github.com/tenable/ghidra_tools
- **gpt-wpre** 🔬 — ingeniería inversa de programa completo con GPT-3. https://github.com/moyix/gpt-wpre
- **burpgpt** 🟢 — extensión de Burp Suite integrando GPT para escaneo pasivo. https://github.com/aress31/burpgpt
- **Burp-extension-for-GPT** 🟢 — extensión de Burp para analizar tráfico HTTP con GPT. (Tenable) https://github.com/tenable/Burp-extension-for-GPT
- **REA** 🟢 — toolkit local CLI/MCP para ingeniería inversa asistida por agente de binarios nativos, archivos PE/CLI gestionados, apps JavaScript/Electron y runtimes de navegador, usando Hopper o una instalación de Ghidra provista por el operador. https://github.com/morluto/rea

---

## 5. AI/ML Supply Chain y Seguridad de Modelos

- **Adversarial Robustness Toolbox (ART)** — ver sección 2.5.
- **modelscan** 🟢 — escanea archivos de modelo ML buscando patrones de serialización insegura y código embebido, enfocado en ataques de serialización de modelos. (Protect AI) https://github.com/protectai/modelscan
- **Fickling** 🟢 — decompilador, reescritor y analizador estático de pickle de Python para inspeccionar y detectar payloads maliciosos de pickle/PyTorch. (Trail of Bits) https://github.com/trailofbits/fickling
- **picklescan** 🟢 — CLI/librería liviana para detectar operaciones sospechosas de pickle de Python en artefactos ML y de modelo. https://github.com/mmaitre314/picklescan
- **AIsbom** 🟢 — herramientas de bill-of-materials de software de IA para inventario y metadatos de proveniencia de supply-chain de IA/ML. https://github.com/Lab700xOrg/aisbom
- **model-provenance-kit** 🟢 — toolkit para proveniencia y fingerprinting de familia de modelos a través de pesos, tokenizadores y señales de arquitectura. (Cisco AI Defense) https://github.com/cisco-ai-defense/model-provenance-kit
- **pickle-fuzzer** 🟢 — fuzzer sensible a la estructura para escáneres de pickle, útil para endurecer herramientas como modelscan, Fickling y picklescan. https://github.com/cisco-ai-defense/pickle-fuzzer
- **Medusa** 🟢⚠️ — escáner de seguridad AI-first para repos IA/ML, agentes y superficies MCP. AGPL-3.0. (Pantheon Security) https://github.com/Pantheon-Security/medusa
- **PrivacyRaven** 🟢🔬 — librería de testing de privacidad para sistemas de deep learning, cubriendo extracción de modelos e inferencia de membresía. Archivado/en pausa. (Trail of Bits) https://github.com/trailofbits/PrivacyRaven
- **gym-malware** 🟢🔬 — entorno OpenAI Gym para agentes de RL que mutan malware PE para evadir detectores estáticos de ML. https://github.com/endgameinc/gym-malware
- **open-malicious-code-benchmark (OMCBench)** 🟢🔬 — suite de benchmark para detección de código/paquete malicioso: archivos etiquetados de Python y JavaScript, runners comunes, métricas precision/recall/F1. https://github.com/False-Positive-Community/open-malicious-code-benchmark
- **malicious-software-packages-dataset** 🟢🔬 — dataset humano-verificado de paquetes de software maliciosos en npm, PyPI, extensiones de IDE y AI Skills. (Datadog Security Labs) https://github.com/DataDog/malicious-software-packages-dataset
- **GuardDog** 🟢 — CLI para detectar paquetes maliciosos de PyPI, npm, Go, RubyGems, GitHub Actions y extensión VSCode usando reglas Semgrep y heurísticas de metadatos. (Datadog) https://github.com/DataDog/guarddog
- **package-analysis** 🟢🔬 — pipeline de análisis estático/dinámico sandboxed para paquetes open-source, capturando comportamiento de filesystem, proceso y red. (OpenSSF) https://github.com/ossf/package-analysis
- **malicious-code-ruleset** 🟢 — ruleset Semgrep enfocado en patrones de código malicioso como ejecución dinámica y ofuscación, usado como baseline de OMCBench. (Apiiro) https://github.com/apiiro/malicious-code-ruleset
- **pypi_malregistry** 🔬⚠️ — dataset de PyPI malicioso ASE'23/USENIX Security'26 con más de 10k versiones de paquete maliciosas. https://github.com/lxyeternal/pypi_malregistry
- **Activation-based Model Scanner (AMS)** 🟢🔬 — escáner PyPI que usa fingerprints de activación relacionados con seguridad para detectar entrenamiento de safety degradado o removido en un modelo. (Google Cloud Platform) *(sin URL propia confirmada en la fuente original)*
- **Snaike-MLflow / Snaike-MLFlow** 🟢 — suite de herramientas de red-team para MLflow. (Protect AI) https://github.com/protectai/Snaike-MLflow
- **Charcuterie** 🟢 — colección de técnicas de ejecución de código dirigidas a librerías ML para evaluación de seguridad. (moohax) https://github.com/moohax/Charcuterie
- **Exploring the Space of Adversarial Images** — herramienta para experimentar con imágenes adversarias. https://github.com/tabacof/adversarial
- **Adversarial Machine Learning Library (Ad-lib)** — librería teoría-de-juegos para ML adversario. https://github.com/vu-aml/adlib
- **EasyEdit** — herramienta para modificar los ground truths de LLMs. https://github.com/zjunlp/EasyEdit
- **BadDiffusion** — repositorio oficial para reproducir el paper "How to Backdoor Diffusion Models?" (CVPR 2023). https://github.com/IBM/BadDiffusion
- **AIJack** — simulador open-source para modelar amenazas de seguridad y privacidad a sistemas ML. (Koukyosyumei) https://github.com/Koukyosyumei/AIJack

---

## 6. Threat Intelligence, SOC/SIEM y DFIR con IA

- **MITRE ATT&CK** — ver sección 1. https://attack.mitre.org/
- **OpenCTI** — plataforma abierta para estructurar y compartir conocimiento de amenazas. *(sin URL propia confirmada en la fuente original)*
- **MISP** — plataforma open-source de threat intelligence para recopilar, compartir, almacenar y correlacionar Indicadores de Compromiso (IoCs). https://www.misp-project.org/
- **ZettelForge** — sistema de memoria agéntica CTI con extracción de entidades (CVEs, actores de amenaza, IOCs, MITRE ATT&CK), grafo de conocimiento con resolución de alias, ontología STIX 2.1, recuperación clasificada por intención y servidor MCP. Offline, MIT. https://github.com/rolandpg/zettelforge
- **Scammer-List** — buscador gratuito de estafas y spam basado en IA con API gratuita. https://scammerlist.now.sh/
- **Sigma** — formato genérico abierto de firmas de detección compartidas.
- **YARA** — coincidencia de patrones basada en reglas para investigación y clasificación.
- **Wazuh** — plataforma open-source XDR/SIEM. https://github.com/wazuh/wazuh
- **Wazuh-MCP-Server** — servidor MCP que expone telemetría SIEM/EDR de Wazuh para hunting y playbooks de respuesta con agentes. https://github.com/gensecaihq/Wazuh-MCP-Server
- **Elastic Detection Rules** — reglas de detección públicas y recursos de desarrollo de reglas.
- **Splunk Boss of the SOC (BOTS) Dataset** — dataset y entorno para práctica de investigación SOC.
- **CTI-Bench / CTIBench** 🔬⚠️ — benchmark spotlight NeurIPS 2024 con 4,610 ejemplos de conocimiento CTI, mapeo de causa raíz CWE, predicción CVSS, extracción de técnica ATT&CK y atribución de actor de amenaza. https://github.com/maveryn/cti-bench · https://huggingface.co/datasets/AI4Sec/cti-bench
- **SECURE** 🟢 — dataset de escenarios de ciberseguridad práctico enfocado en extracción, comprensión y razonamiento; benchmark orientado a Industrial Control Systems. https://github.com/aiforsec/SECURE
- **trs** 🟢 — herramienta LLM + ChromaDB para resumir reportes de amenazas y extraer TTPs e IOCs de MITRE. https://github.com/deadbits/trs
- **TI-Mindmap-GPT** 🟢 — app Streamlit: resúmenes de IA, mindmaps, extracción de IOC/TTP y capas de ATT&CK Navigator. https://github.com/format81/TI-Mindmap-GPT
- **aiocrioc** 🟢 — extracción de IOC con LLM + OCR (extrae IOCs de imágenes/PDFs). https://github.com/referefref/aiocrioc
- **ThreatIngestor** 🟢 — extrae/agrega IOCs de feeds; se integra con MISP/ThreatKB. https://github.com/InQuest/ThreatIngestor
- **IATelligence** 🟢 — explica APIs de Windows importadas en archivos PE vía GPT y mapea a MITRE ATT&CK. https://github.com/fr0gger/IATelligence
- **threat-intelligence-cti-analysis** 🟢 — pipeline NLP/LLM para extracción de IOC, mapeo MITRE ATT&CK y generación de knowledge-graph desde CTI no estructurada. https://github.com/AnandBinuArjun/threat-intelligence-cti-analysis
- **CTINexus** 🟢🔬 — framework asistido por LLM para extracción eficiente de datos de threat intelligence y construcción de knowledge graphs de ciberseguridad estructurados desde reportes no estructurados. https://github.com/peng-gao-lab/ctinexus
- **CTI-BERT** 🟢🔬 — modelo BERT preentrenado desde cero en un gran corpus de texto de ciberseguridad para extracción, clasificación y Q&A de CTI. (IBM Research) https://huggingface.co/ibm-research/CTI-BERT
- **AI-SOC-Agent** 🟢 — servidor MCP de Black Hat 2025 que expone herramientas de investigación de seguridad (ELK, IRIS). https://github.com/M507/ai-soc-agent
- **soctalk** 🟢 — agente de automatización SOC LangGraph con integraciones MCP para Wazuh, Cortex, TheHive y MISP, más lab de test con agentes simulados. https://github.com/soctalk/soctalk
- **Vigil SOC** 🟢 — SOC de IA open-source con agentes Python legibles, playbooks Markdown e integraciones MCP para triage, investigación, hunting, respuesta, reporting y forense. https://github.com/Vigil-SOC/vigil
- **agentic-soc-platform** 🟢 — plataforma SOC agéntica (LangGraph/Dify) con soporte de LLM local. https://github.com/FunnyWolf/agentic-soc-platform
- **SigmAIQ** 🟢⚠️ — wrapper pySigma y toolkit LangChain para creación y traducción automática de reglas Sigma; LGPL-2.1. (AttackIQ) https://github.com/AttackIQ/SigmAIQ
- **RulePilot** 🟢🔬 — agente de generación de reglas de seguridad impulsado por LLM para Splunk, Microsoft Sentinel y Elastic. https://github.com/LLM4SOC-Topic/RulePilot
- **SOCGPT** 🟢 — resumen de logs con LLM, triage de severidad, mapeo MITRE y Q&A. https://github.com/Ninadjos/SOCGPT-AI-Powered-SOC-Assistant
- **AttackGen** 🟢 — generador de escenarios de respuesta a incidentes dirigido por LLM usando MITRE ATT&CK + ATLAS. https://github.com/mrwadams/attackgen
- **Google Security Operations and Threat Intelligence MCP Server** — ver sección 2.4.
- **ExCyTIn-Bench (SecRL)** 🟢🔬 — benchmark ICML 2026 para evaluar agentes LLM en investigación de amenazas cibernéticas y threat hunting mediante Q&A de seguridad sobre ocho bases de datos de incidentes anonimizadas. (Microsoft) https://github.com/microsoft/SecRL
- **Cortex** — motor flexible y poderoso de análisis de observables y respuesta activa; la IA puede automatizar el análisis de observables. (TheHive Project) https://github.com/TheHive-Project/Cortex
- **MemoryInvestigator** 🔬 — Volatility 3 + LLM + RAG para triage forense de memoria. *(sin URL propia confirmada en la fuente original)*
- **Volatility-MCP-Server** 🟢 — MCP que expone plugins de Volatility 3 para forense de memoria en lenguaje natural. *(sin URL propia confirmada en la fuente original)*
- **EscalateGPT** 🟢 — descubrimiento basado en GPT de rutas de escalación de privilegios en políticas IAM de AWS. (Tenable) https://github.com/tenable/EscalateGPT
- **Julius** 🟢 — herramienta Go local que hace fingerprinting de infraestructura de servicio LLM en endpoints autorizados, identifica 60+ plataformas de serving, gateway, MCP y RAG. (Praetorian) *(sin URL propia confirmada en la fuente original)*

---

## 7. Modelos de IA Especializados en Ciberseguridad

- **Foundation-Sec-8B** — modelo base de 8B parámetros con preentrenamiento específico de ciberseguridad, superando a Llama 3.1 70B en tareas de threat intelligence con 10x menos parámetros. https://huggingface.co/fdtn-ai/Foundation-Sec-8B
- **Foundation-Sec-8B-Instruct** — modelo de 8B ajustado por instrucciones, diseñado como copiloto chat-native para workflows de ciberseguridad. https://huggingface.co/fdtn-ai/Foundation-Sec-8B-Instruct
- **Foundation-Sec-8B-Reasoning** — extiende Foundation-Sec-8B con capacidades de razonamiento, logrando estado del arte en benchmarks CTI. https://huggingface.co/fdtn-ai/Foundation-Sec-8B-Reasoning
- **Foundation-Sec-1.1-8B-Instruct** — último modelo de 8B con ventana de contexto extendida de 64k. https://huggingface.co/fdtn-ai/Foundation-Sec-1.1-8B-Instruct
- **Foundation-Sec Technical Report** — metodología detallada de domain-adaptation de Llama-3.1 para ciberseguridad. https://huggingface.co/fdtn-ai/Foundation-Sec-8B/blob/main/Technical_Report.pdf
- **Antares-1B** — SLM de seguridad de peso abierto especializada en localización agéntica de vulnerabilidades; explora snapshots de repositorio a través de un loop estilo terminal. Licencia Apache-2.0, acceso gated manual. (Cisco Foundation AI) https://huggingface.co/fdtn-ai/antares-1b
- **Antares-350M** — agente terminal de 350M parámetros para localización de vulnerabilidades, suficientemente pequeño para correr solo en CPU. https://huggingface.co/fdtn-ai/antares-350m
- **Llama-Primus-Base** — modelo fundacional con preentrenamiento específico de ciberseguridad en corpus propietario. https://huggingface.co/trendmicro-ailab/Llama-Primus-Base
- **Llama-Primus-Merged** — modelo combinado mediante preentrenamiento y fine-tuning por instrucciones. https://huggingface.co/trendmicro-ailab/Llama-Primus-Merged
- **Llama-Primus-Reasoning** — modelo especializado en razonamiento que mejora la certificación de seguridad mediante patrones de razonamiento destilados de o1. https://huggingface.co/trendmicro-ailab/Llama-Primus-Reasoning
- **Primus Paper** — primera colección de datasets de ciberseguridad open-source que aborda la escasez crítica de corpus de preentrenamiento. https://arxiv.org/abs/2502.11191
- **SecureBERT** — modelo de la familia BERT para tareas de texto de ciberseguridad. *(sin URL propia confirmada en la fuente original)*
- **HackMentor** — repositorio histórico que separa construcción de datos, entrenamiento y evaluación para un LLM de ciberseguridad. *(sin URL propia confirmada en la fuente original)*
- **SecGPT** 🟢 — familia de LLMs open-source ajustados a ciberseguridad para análisis de vulnerabilidades, investigación de logs/tráfico, detección de anomalías, razonamiento ataque/defensa, análisis de comandos y Q&A de seguridad. (Clouditera) https://github.com/Clouditera/secgpt
- **Trendyol Cybersecurity LLM v2 70B** — LLM de ciberseguridad enfocado en defensa basado en Llama-3.3-70B, entrenado en un dataset de instrucciones de seguridad alignment-safe. Licencia Apache-2.0. https://huggingface.co/Trendyol/Trendyol-Cybersecurity-LLM-v2-70b
- **WhiteRabbitNeo 2.5 Qwen Coder 7B** ⚠️ — fine-tune orientado a ciberseguridad de Qwen2.5-Coder para asistencia ofensiva y defensiva. Licencia Apache-2.0 + restricciones WhiteRabbitNeo. *(sin URL propia confirmada en la fuente original)*
- **Lily-Cybersecurity-7B-v0.2** — fine-tune de Mistral-7B-Instruct para asistencia de ciberseguridad. Licencia Apache-2.0. (Segolily Labs) *(sin URL propia confirmada en la fuente original)*
- **RavenX CyberAgent 35B Q4_K_M** ⚠️ — modelo GGUF especializado en seguridad posicionado para pentesting, bug-bounty, tool-calling, MCP, CVSS/CWE y MITRE ATT&CK. Construido sobre un modelo base "abliterated"; usar solo en harnesses de agente sandboxed con validación de tool-call. (RavenX LLC / DeadByDawn101) *(sin URL propia confirmada en la fuente original)*

---

## 8. Datasets para Entrenamiento y Evaluación

- **Primus-FineWeb** — corpus filtrado de ciberseguridad (2.57B tokens) derivado de FineWeb usando selección basada en clasificador. https://huggingface.co/datasets/trendmicro-ailab/Primus-FineWeb
- **Primus-Reasoning** — tareas de razonamiento de ciberseguridad con pasos de razonamiento generados por o1. https://huggingface.co/datasets/trendmicro-ailab/Primus-Reasoning
- **Primus-Instruct** — instrucciones de escenarios de ciberseguridad curadas por expertos con respuestas generadas por GPT-4o. https://huggingface.co/datasets/trendmicro-ailab/Primus-Instruct
- **AI AppSec Index** — referencia open-source con 6 datasets estructurados cubriendo benchmarks de remediación IA, matriz de vendors ASPM, 48+ CVEs reales en código generado por IA, mapeo de cumplimiento EU CRA y tasas de falsos positivos SAST. https://github.com/alpha-one-index/ai-appsec-index
- **malicious-software-packages-dataset / pypi_malregistry** — ver sección 5.
- **JailbreakLLMs / In-The-Wild Jailbreak Prompts Dataset / JailBreakV-28K / Forbidden Question Set / Do-Not-Answer** — ver sección 2.6.
- **LLM Jailbreak + Safety Data** — ~10K ejemplos de fine-tuning y ~3K prompts adversarios para safety de chatbots. https://www.kaggle.com/datasets/llm-jailbreak-safety
- **TruthfulQA** — veracidad bajo conceptos erróneos. https://github.com/sylinrl/TruthfulQA
- **ToxiGen** — dataset y benchmarks de toxicidad. https://github.com/microsoft/TOXIGEN
- **MMLU Computer Security** — subconjunto estándar de evaluación de seguridad informática de MMLU. https://huggingface.co/datasets/cais/mmlu/viewer/computer_security
- **MMLU Security Studies** — subconjunto de estudios de seguridad de MMLU. https://huggingface.co/datasets/cais/mmlu/viewer/security_studies

---

## 9. Benchmarks, Cyber Ranges y Marcos de Evaluación

Un puntaje de benchmark solo es significativo cuando se conocen la tarea, el modelo, el scaffold del agente, las herramientas, el entorno, los intentos y el presupuesto — no se deben comparar resultados white-box y black-box como si fueran equivalentes.

- **CyBench** — 40 tareas CTF profesionales en 4 competencias; ampliamente usado por institutos de seguridad de IA. Ver también sección 3.6.
- **CyberGym** — evaluación a gran escala de análisis de vulnerabilidades de agentes de IA en tareas reales; abstract reporta ~20% de éxito incluso para las mejores combinaciones evaluadas.
- **NYU CTF Bench** — desafíos CTF Dockerizados para evaluación controlada de agentes LLM. https://github.com/NYU-LLM-CTF/NYU_CTF_Bench
- **CyberSecEval / CyberSecEval 4** — suite de benchmark integral para evaluar vulnerabilidades de ciberseguridad de LLM con evaluaciones multi-vendor. https://meta-llama.github.io/PurpleLlama/CyberSecEval/docs/intro
- **SecBench** — dataset de benchmark de conocimiento de seguridad más completo, distinguiendo entre preguntas de conocimiento y razonamiento. https://huggingface.co/datasets/secbench-hf/SecBench
- **CVE-Bench** — aplicaciones web vulnerables y CVEs para evaluación controlada de agentes. Ver sección 3.6.
- **BountyBench** — 25 sistemas reales / 40 bug bounties para evaluación Detect-Exploit-Patch.
- **AgentCyberRange** — infraestructura de investigación abierta de cyber-range para evaluar agentes en escenarios aislados multi-host de explotación web y post-explotación.
- **AISI multi-step cyber-range study** — estudio controlado de rendimiento en cyber-range multi-paso.
- **AI Cyber Model Arena** — evaluación matriz de agente/modelo de Wiz Research a través de dominios reales en contenedores aislados.
- **BotsBench** — evaluación de agentes en tareas de investigación de operaciones de seguridad.
- **DefenseBench** — evaluación de agentes en operaciones de ciberseguridad defensiva.
- **SecLLMHolmes** — ver sección 4.1.
- **AutoPatchBench / VLoc Bench** — ver sección 4.1.
- **AIxCC** — ver sección 3.3 (54 vulnerabilidades sintéticas encontradas de 63, 43 parcheadas, en la final de DARPA).
- **Practical AI Security Course** — curso de seguridad de IA/LLM enfocado en aplicar IA/LLMs a problemas de seguridad y crear agentes de pentesting. https://academy.8ksec.io/course/practical-ai-security

---

## 10. Sandboxing de Agentes de IA

Los agentes de codificación de IA son útiles precisamente porque pueden leer archivos, ejecutar comandos, instalar paquetes, abrir conexiones de red y modificar código — lo cual también los hace riesgosos.

**Aislamiento a nivel de host (multiplataforma):**

- **cage** — ejecuta agentes de codificación en contenedores Docker aislados en macOS o Linux. https://github.com/pacificsky/cage
- **agent-sandbox.nix** — wrappers Nix para ejecución CLI de IA restringida con permisos explícitos de paquete y red. https://github.com/archie-judd/agent-sandbox.nix
- **cco** — lanzador delgado que elige un backend de sandbox local. https://github.com/nikvdp/cco
- **nixcage** — sandboxing de entorno Nix con `bubblewrap` en Linux y `sandbox-exec` en macOS. https://github.com/hamidr/nixcage
- **Pent** — sandbox de proceso OS nativo para comandos no confiables. https://github.com/valentinradu/pent
- **Sandbox Runtime (Anthropic)** — capa de restricción de filesystem y red a nivel OS sin contenedores. https://github.com/anthropic-experimental/sandbox-runtime
- **sandnix** — módulo Nix para envolver programas con Landlock o `sandbox-exec`. https://github.com/srid/sandnix
- **workmux** — aislamiento de workflow con Git worktree y `tmux`. https://github.com/raine/workmux
- **yoloAI** — runner local multi-backend (Seatbelt, Tart o Docker) con workflow review/apply. https://github.com/kstenerud/yoloai

**macOS:**

- **Agent Safehouse** — sistema de perfiles Seatbelt deny-first para agentes de codificación locales. https://github.com/eugene1g/agent-safehouse
- **sandbox-shell** — wrapper de shell Seatbelt para acceso deny-by-default. https://github.com/agentic-dev3o/sandbox-shell
- **SandVault** — ejecuta agentes en una cuenta de usuario macOS separada con endurecimiento `sandbox-exec`. https://github.com/webcoyote/sandvault
- **vibebox** — sandbox macOS local rápido orientado a uso de agentes IA. https://github.com/robcholz/vibebox
- **yolobox** — sandbox local enfocado en dejar trabajar a los agentes sin exponer todo el home directory. https://github.com/finbarr/yolobox

**Linux:**

- **sandlock** — confina código no confiable usando Landlock, seccomp-bpf y notificación de usuario seccomp. https://github.com/multikernel/sandlock
- **Fence** — sandbox de comandos nativo para restricciones de filesystem y red sin contenedores. https://github.com/use-tusk/fence
- **Matchlock** — sandbox Linux orientado a asegurar workloads de agente IA. https://github.com/jingkaihe/matchlock
- **Microbox** — sandboxes Linux efímeros livianos. https://github.com/hqarroum/microbox
- **Nono** — sandbox respaldado por kernel orientado a capacidades para ejecución de agente. https://github.com/always-further/nono
- **sandbox-run** — wrapper basado en `bubblewrap` para aislamiento de comandos Linux por proyecto. https://codeberg.org/Grauwolf/sandbox-run
- **sandbox-runtime** — sandbox de proceso liviano para enforcement de política de filesystem y red. https://github.com/carderne/sandbox-runtime
- **shai** — shell de sandboxing para agentes de codificación IA. https://github.com/colony-2/shai
- **sucoder** — enfoque basado en permisos Unix para contener agentes de codificación. https://github.com/ligon/sucoder
- **treebeard** — sandbox de Git worktree efímero con manejo copy-on-write y restricciones de red opcionales. https://github.com/divmain/treebeard

**Máquinas virtuales y plataformas microVM (multiplataforma):**

- **boxed** — motor de ejecución de código para código de agente no confiable a través de Docker, Firecracker y Wasm. https://github.com/akshayaggarwal99/boxed
- **BoxLite** — sandboxing estilo VM embebible con snapshots y estado persistente. https://github.com/boxlite-ai/boxlite (implementación relacionada: https://github.com/boxlite-labs/boxlite)
- **coderunner** — runner de sandbox estilo hospedado para código IA no confiable. https://github.com/instavm/coderunner
- **K7** — infraestructura de sandbox VM liviana self-hosted con API y SDK. https://github.com/katakate/k7
- **smolVM** — gestor de microVM local para workloads aislados efímeros y persistentes. https://github.com/smol-machines/smolvm

**macOS (VM):**

- **Chamber** — runner de VM macOS efímero basado en Tart para Claude o Codex. https://github.com/cirruslabs/chamber
- **ClodPod** — workflow de VM macOS que mapea proyectos del host a un entorno guest. https://github.com/webcoyote/clodpod
- **lima-devbox** — workflow de sandbox de desarrollo VM basado en Lima para Mac. https://github.com/recodelabs/lima-devbox

**Linux (VM):**

- **agentsafe** — sandbox microVM por tarea para agentes de IA. https://github.com/sarthak30/agentsafe
- **avkcode/firecracker-sandbox** — experimento de sandbox basado en Firecracker. https://github.com/avkcode/firecracker-sandbox
- **bunkervm** — entorno VM Linux diminuto posicionado como máquina segura simple para agentes. https://github.com/ashishgituser/bunkervm
- **Cleanroom** — sandbox microVM self-hosted con egreso deny-by-default y proxy de credenciales. https://github.com/buildkite/cleanroom
- **hhtpcd/firecracker-sandbox** — otra implementación de sandbox Firecracker. https://github.com/hhtpcd/firecracker-sandbox
- **nervos** — sandbox microVM Firecracker para agentes de IA. https://github.com/ashishgituser/nervos
- **python-firecracker** — interfaz Python para Firecracker, no un producto completo de sandbox de agente. https://github.com/okeso/python-firecracker

**Contenedores, LXC y runtimes empaquetados (multiplataforma):**

- **agentbox** — sandbox de agente contenerizado con firewalling de red y drop de privilegios. https://github.com/gbrindisi/agentbox
- **AIO Sandbox** — sandbox Docker completo con shell, navegador, archivos, Jupyter, VS Code server y MCP. https://github.com/agent-infra/sandbox
- **Amazing Sandbox** — sandbox local general para herramientas de terceros y agentes de IA. https://github.com/ashishb/amazing-sandbox
- **claude-code-devcontainer** — plantilla de devcontainer endurecida. (Trail of Bits) https://github.com/trailofbits/claude-code-devcontainer
- **ClaudeBox** — entorno Claude Code basado en Docker con estado persistente y allowlists. https://github.com/RchGrav/claudebox
- **codex-lockbox** — sandbox Docker enfocado en ejecutar Codex CLI detrás de reglas de firewall. https://github.com/paulux84/codex-lockbox
- **conch** — enfoque de sandbox estilo Wasm/bash para ejecución de comandos de agente. https://github.com/sd2k/conch
- **EdgeBox** — sandbox GUI local que expone un escritorio al agente. https://github.com/bigppwong/edgebox
- **Kilntainers** — runtime de sandbox orientado a MCP respaldado por Docker, Podman, microVMs o Wasm. https://github.com/Kiln-AI/Kilntainers
- **packnplay** — sandbox de comandos respaldado por Docker con gestión de worktree y dev-container. https://github.com/obra/packnplay
- **sandclaude** — wrapper Docker opinionado para Claude Code. https://github.com/binwiederhier/sandclaude
- **Sculptor** — herramientas de escritorio para ejecutar agentes dentro de contenedores aislados y testear cambios. https://github.com/imbue-ai/sculptor

**Linux (contenedores):**

- **Greywall** — sandbox local con control de red en vivo y funciones de visibilidad. https://github.com/greyhavenhq/greywall
- **runbox** — implementación de sandbox mínima estilo contenedor en C. https://github.com/sahilb315/runbox
- **sbox** — proyecto de sandbox pequeño enfocado en aislamiento. https://github.com/cvpaul/sbox
- **vibebin** — plataforma Incus/LXC para sandboxes de agente de codificación self-hosted persistentes. https://github.com/jgbrwn/vibebin

**Políticas, aprobaciones y capas de auditoría:**

- **claude-rule-enforcer** — restricción y enforcement de reglas en torno al comportamiento de Claude Code. https://github.com/tech-and-ai/claude-rule-enforcer
- **Cupcake** — enforcement de hooks basado en OPA/Rego para agentes de codificación. https://github.com/eqtylab/cupcake
- **deepclause-sdk** — SDK de política/runtime para lógica de autorización estilo DML. https://github.com/deepclause/deepclause-sdk
- **nah** — guardia determinístico allow/ask/block para tool calls de Claude Code. https://github.com/manuelschipper/nah
- **predicate-secure** — autorización basada en política y verificación post-ejecución para agentes. https://github.com/PredicateSystems/predicate-secure
- **punkgo-jack** — capa de auditoría y recibos para acciones de agente vía eventos hook Merkle-logged. https://github.com/PunkGo/punkgo-jack
- **shannot** — flujo de ejecución y aprobación human-in-the-loop para agentes LLM. https://github.com/corv89/shannot
- **firewarden** — abre archivos dentro de sandboxes Firejail privados. https://github.com/pigmonkey/firewarden

**Primitivas de sandbox de bajo nivel:**

- **agentfs** — capa de filesystem orientada a agentes. https://github.com/tursodatabase/agentfs
- **bubblewrap** — constructor de sandbox de namespace/filesystem Linux central. https://github.com/containers/bubblewrap
- **bVisor** — sandbox bash embebido inspirado en gVisor. https://github.com/butter-dot-dev/bvisor
- **firecracker-go-sdk** — SDK Go para ensamblar runtimes respaldados por Firecracker. https://github.com/firecracker-microvm/firecracker-go-sdk
- **Firejail** — sandbox Linux maduro para escritorio/aplicaciones usando namespaces y seccomp. https://github.com/netblue30/firejail
- **gVisor** — frontera kernel de espacio de usuario/application-kernel usada para endurecer ejecución contenerizada. (Google) https://github.com/google/gvisor
- **island** — CLI de sandbox Linux potenciado por Landlock. https://github.com/landlock-lsm/island
- **libkrun** — runtime de virtualización liviano usado frecuentemente bajo sistemas de sandbox de más alto nivel. https://github.com/containers/libkrun
- **Minijail** — lanzador y librería de contención de ChromeOS/Android. (Google) https://github.com/google/minijail
- **sacre_bleu** — suite de generación, inyección y enforcement de políticas seccomp y Landlock para binarios Linux. https://github.com/hsaliak/sacre_bleu
- **syd** — sandbox Linux de interceptación de syscall en espacio de usuario. https://git.sr.ht/~alip/syd

**Perfiles, plantillas y ayudantes operacionales:**

- **ansible-firejail** — automatización Ansible para desplegar perfiles Firejail. https://github.com/debops-contrib/ansible-firejail
- **bubblewrap-tui** — UI de terminal para construir líneas de comando Bubblewrap. https://github.com/reubenfirmin/bubblewrap-tui
- **firejail-profiles** — colección de perfiles para setups de sandbox basados en Firejail. https://github.com/chiraag-nataraj/firejail-profiles
- **firetools** — compañero GUI para trabajar con sandboxes Firejail. https://github.com/netblue30/firetools

**Sistemas de agente adyacentes y experimentos especializados:**

- **ash-ai, bouvet, cagent, co-do, construct-cli, forgemax, litterbox, microsandbox (exploración), OmniGlass, qonqrete, rcarmo/agentbox, selenai, SkillSandbox, smith-core, tsk, voratiq, VTCode, YourOwnPersonalJean-Luc, zapcode** — colección de sistemas de agente experimentales/adyacentes al sandboxing, cada uno con distinto grado de madurez; ver https://github.com/webcoyote/awesome-AI-sandbox#adjacent-agent-systems-and-specialized-experiments para el listado completo con enlaces individuales.

**Referencias:**

- **Awesome Agent Sandboxes** — lista curada enfocada en sandboxes de ejecución IA/LLM. https://github.com/arjan/awesome-agent-sandboxes
- **Awesome Sandbox** — panorama amplio de tecnologías y plataformas de sandboxing. https://github.com/restyler/awesome-sandbox
- **Sandbox Probe** — sonda Go estática que mide las capacidades efectivas de filesystem, red, proceso, credenciales y runtime expuestas dentro de un sandbox de agente IA. (ControlPlane) *(sin URL propia confirmada en la fuente original)*

---

## 11. OSINT, Cloud/IaC y Phishing con IA

- **ai_osint** 🟢 — dorks, queries y técnicas de OSINT-IA curadas para descubrir infraestructura LLM/IA expuesta. https://github.com/pikpikcu/ai_osint
- **llm_osint** 🟢🔬 — framework proof-of-concept de OSINT con LLM usando agentes de conocimiento y web para workflows de investigación en internet. https://github.com/aidenybai/llm_osint
- **PhishLLM** 🔬⚠️ — detección de phishing sin referencia vía reconocimiento de marca por LLM (USENIX'24). *(sin URL propia confirmada en la fuente original)*
- **PhishIntention** 🔬 — detector de phishing de deep-vision que infiere tanto la intención de marca como la intención de robo de credenciales a partir de la apariencia y dinámica de la página web (USENIX Security 2022). Licencia CC0-1.0. https://github.com/lindsey98/PhishIntention
- **VisualPhishNet** 🔬⚠️ — CNN triplete para detección de phishing de día cero por similitud visual a sitios confiables (ACM CCS 2020). (CISPA) https://github.com/S-Abdelnabi/VisualPhishNet
- **phishing-url-detection** 🟢 — clasificador de phishing de URL empaquetado con artefactos ONNX y pickle. Licencia MIT. https://huggingface.co/pirocheto/phishing-url-detection
- **Phishing Email Detection DistilBERT v2.4.1** 🟢 — modelo de clasificación de texto DistilBERT para detección de phishing de email y URL. Licencia Apache-2.0. https://huggingface.co/cybersectony/phishing-email-detection-distilbert_v2.4.1
- **mcp-dnstwist** 🟢 — servidor MCP para fuzzing de DNS con dnstwist, para análisis de typosquatting, phishing y dominios look-alike. https://github.com/BuStudios/mcp-dnstwist
- **osintgpt** 🟢⚠️ — embeddings de OpenAI + Qdrant sobre corpus OSINT. https://github.com/afaqueumer/osintgpt
- **Cynative** — ver sección 3.2 (CLI de investigación de seguridad IA local para cloud, código y entornos runtime).
- **EscalateGPT** — ver sección 6 (descubrimiento de rutas de escalación de privilegios AWS IAM basado en GPT).
- **AI-Goat (Orca Security)** — ver sección 3.6 (lab AWS/Terraform deliberadamente vulnerable).

---

## 12. Machine Learning "Clásico" aplicado a Seguridad (pre-LLM)

Organizado por el modelo PPDR de Gartner (Prediction, Prevention, Detection, Response) y capa técnica (Network, Endpoint, Application, User, Process behavior).

**Predicción — Red:**
- **Continuous CyberBattleSim** — ver sección 3.2.
- **open-appsec** — motor de seguridad open-source de machine learning que previene preventiva y automáticamente amenazas contra Web Applications & APIs. https://github.com/openappsec/openappsec

**Predicción — Malware:**
- **OpenVAS** — escáner y solución de gestión de vulnerabilidades open-source; la IA puede mejorar la identificación y priorización de vulnerabilidades. https://www.openvas.org/
- **SEMA** — toolchain usando ejecución simbólica para análisis de malware, construye grafos de dependencia de syscalls (SCDGs) para clasificación. https://github.com/csvl/SEMA-ToolChain
- **Malware environment for OpenAI Gym** — crea una IA que aprende por RL qué transformaciones hacer en una muestra de malware para evadir detección estática ML. https://github.com/endgameinc/gym-malware

**Prevención — Red:**
- **Snort IDS** — IDS/IPS de red open-source con análisis de tráfico en tiempo real; la IA puede mejorar la detección de anomalías. https://www.snort.org/
- **PANTHER** — combina verificación formal de protocolos de red integrando el simulador Shadow con la herramienta de verificación formal Ivy; simula APTs en protocolos de red. https://github.com/ElNiak/PANTHER

**Prevención — Endpoint:**
- **OSSEC** — HIDS open-source; la IA puede mejorar la detección de anomalías y análisis predictivo. https://www.ossec.net/

**Detección — Red:**
- **Zeek** — framework de análisis de red enfocado en monitoreo de seguridad. https://github.com/zeek/zeek
- **AIEngine** — motor de inspección de paquetes interactivo/programable de próxima generación con funcionalidad IDS. https://github.com/camp0/aiengine
- **Security Anomaly ML** — detector de flujo de red ML open-source que convierte tráfico compatible con CICFlowMeter en incidentes de seguridad determinísticos para analistas. https://github.com/ibondarenko1/security-anomaly-ml

**Detección — Endpoint:**
- **Sophos Intercept X** — protección de endpoint avanzada combinando detección basada en firmas con análisis conductual impulsado por IA. https://www.sophos.com/en-us/products/intercept-x.aspx
- **MARK** — framework multi-agente de ranking para construir sistemas de detección y ranking a gran escala, con almacenamiento distribuido y motor de ejecución para algoritmos de detección. https://gitlab.cylab.be/cylab/mark

**Respuesta — Red:**
- **Metasploit** — herramienta para desarrollar y ejecutar código de exploit contra una máquina objetivo remota; la IA puede automatizar la selección de exploits. https://www.metasploit.com/
- **PentestGPT (versión hackerai-tech)** — ver sección 3.2.

**Respuesta — Endpoint:**
- **Cortex** — ver sección 6.

**Monitoreo/Escaneo — Red:**
- **Nmap** — escáner de red gratuito y open-source para descubrir hosts y servicios; la IA puede automatizar el análisis de resultados de escaneo. https://nmap.org

**Monitoreo/Escaneo — Endpoint:**
- **Burp Suite** — suite líder de herramientas de ciberseguridad de PortSwigger; puede integrar IA para automatizar detección de vulnerabilidades. https://portswigger.net/burp
- **Nikto** — escáner de servidor web open-source que realiza pruebas exhaustivas contra servidores web. https://github.com/sullo/nikto

**Usuario:**
- **MISP** — ver sección 6.
- **ZettelForge** — ver sección 6.
- **Scammer-List** — ver sección 6.

**Comportamiento de proceso (detección de fraude):** basado en regresión/clasificación/clustering para detectar anomalías en procesos de negocio; ver papers relacionados en la sección 13.

**Best practices y casos de estudio de seguridad de IA en SaaS:**
- **NIST AI RMF** — ver sección 1.
- **Microsoft AI Security** — casos de estudio sobre asegurar aplicaciones de IA en entornos SaaS. https://www.microsoft.com/en-us/security/ai
- **Google AI Security** — insights y casos de estudio de Google sobre cómo asegurar aplicaciones de IA en la nube. https://cloud.google.com/security/ai
- **IBM Watson (seguridad)** — herramientas y soluciones para asegurar aplicaciones de IA, analiza grandes volúmenes de datos de seguridad. https://www.ibm.com/security/artificial-intelligence
- **Azure Security Center** — sistema de gestión de seguridad integral para entornos cloud usando IA/ML para identificar amenazas en tiempo real. https://azure.microsoft.com/en-us/services/security-center/
- **OneCLI** — bóveda de credenciales open-source para agentes de IA; gateway HTTP en Rust que intercepta requests de agente e inyecta claves API de forma transparente. https://github.com/onecli/onecli
- **Xquik** — API independiente de datos de X (Twitter) para búsqueda, exportación de seguidores, monitores y MCP. https://github.com/Xquik-dev/x-twitter-scraper

---

## 13. Papers de Investigación

Organizados por categoría. La mayoría provienen de `ElNiak/awesome-ai-cybersecurity` y `EvanThomasLuke/Awesome-AI-Hacking-Agents`.

**Ataques y hacking ofensivo con agentes LLM:**

- Teams of LLM Agents can Exploit Zero-Day Vulnerabilities — https://alphaxiv.org/abs/2406.01637
- LLM Agents can Autonomously Hack Websites — https://alphaxiv.org/abs/2402.06664
- RedTeamLLM: an Agentic AI framework for offensive security — https://alphaxiv.org/abs/2505.06913
- Incalmo: An Autonomous LLM-assisted System for Red Teaming Multi-Host Networks — https://alphaxiv.org/abs/2501.16466
- HackSynth: LLM Agent and Evaluation Framework for Autonomous Penetration Testing — https://alphaxiv.org/abs/2412.01778
- LLMs as Hackers: Autonomous Linux Privilege Escalation Attacks — https://alphaxiv.org/abs/2310.11409
- LLM Agents can Autonomously Exploit One-day Vulnerabilities — https://alphaxiv.org/abs/2404.08144
- CVE-Bench: A Benchmark for AI Agents' Ability to Exploit Real-World Web Application Vulnerabilities — https://alphaxiv.org/abs/2503.17332
- Getting pwn'd by AI - Penetration Testing with Large Language Models — https://arxiv.org/abs/2308.00121
- Evaluating LLMs for Privilege-Escalation Scenarios — https://arxiv.org/abs/2310.11409
- A Study on Robustness and Reliability of Large Language Model Code Generation — https://arxiv.org/abs/2308.10335
- Summoning Demons - The Pursuit of Exploitable Bugs in Machine Learning — https://arxiv.org/abs/1701.04739
- capAI - A Procedure for Conducting Conformity Assessment of AI Systems in Line with the EU Artificial Intelligence Act — https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4064091

**Ejemplos y ataques adversarios (visión/general):**

- High Dimensional Spaces, Deep Learning and Adversarial Examples — https://arxiv.org/abs/1801.00634
- Adversarial Task Allocation — https://arxiv.org/abs/1709.00358
- Robust Physical-World Attacks on Deep Learning Models — https://arxiv.org/abs/1707.08945
- The Space of Transferable Adversarial Examples — https://arxiv.org/abs/1704.03453
- RHMD - Evasion-Resilient Hardware Malware Detectors — http://www.cs.ucr.edu/~kkhas001/pubs/micro17-rhmd.pdf
- Vulnerability of Deep Reinforcement Learning to Policy Induction Attacks — https://arxiv.org/abs/1701.04143
- Can you fool AI with adversarial examples on a visual Turing test? — https://arxiv.org/abs/1709.08693
- Explaining and Harnessing Adversarial Examples — https://arxiv.org/abs/1412.6572
- Delving into Adversarial Attacks on Deep Policies — https://arxiv.org/abs/1705.06452
- Crafting Adversarial Input Sequences for Recurrent Neural Networks — https://arxiv.org/abs/1604.08275
- Practical Black-Box Attacks against Machine Learning — https://arxiv.org/abs/1602.02697
- Generating Adversarial Malware Examples for Black-Box Attacks Based on GAN — https://arxiv.org/abs/1702.05983
- Data Driven Exploratory Attacks on Black Box Classifiers in Adversarial Domains — https://arxiv.org/abs/1703.07909
- Fast Feature Fool - A Data-Independent Approach to Universal Adversarial Perturbations — https://arxiv.org/abs/1707.05572v1
- Simple Black-Box Adversarial Perturbations for Deep Networks — https://arxiv.org/abs/1612.06299
- Wild Patterns - Ten Years After the Rise of Adversarial Machine Learning — https://arxiv.org/abs/1712.03141
- One Pixel Attack for Fooling Deep Neural Networks — https://arxiv.org/abs/1710.08864v1
- FedMLSecurity - A Benchmark for Attacks and Defenses in Federated Learning and LLMs — https://arxiv.org/abs/2306.04959
- Jailbroken - How Does LLM Safety Training Fail? — https://arxiv.org/abs/2307.02483
- Bad Characters - Imperceptible NLP Attacks — https://arxiv.org/abs/2106.09898
- Universal and Transferable Adversarial Attacks on Aligned Language Models — https://arxiv.org/abs/2307.15043
- Exploring the Vulnerability of Natural Language Processing Models via Universal Adversarial Texts — https://aclanthology.org/2021.alta-1.14/
- Adversarial Examples Are Not Bugs, They Are Features — https://arxiv.org/abs/1905.02175
- Adversarial Attacks on Tables with Entity Swap — https://ceur-ws.org/Vol-3462/TADA4.pdf
- Here Comes the AI Worm - Unleashing Zero-click Worms that Target GenAI-Powered Applications — https://arxiv.org/abs/2403.02817

**Extracción de modelos:**

- Stealing Machine Learning Models via Prediction APIs — https://arxiv.org/abs/1609.02943
- On the Risks of Stealing the Decoding Algorithms of Language Models — https://arxiv.org/abs/2303.04729

**Evasión:**

- Adversarial Demonstration Attacks on Large Language Models — https://arxiv.org/abs/2305.14950
- Looking at the Bag is not Enough to Find the Bomb — https://pralab.diee.unica.it/sites/default/files/maiorca_ASIACCS13.pdf
- Adversarial Generative Nets - Neural Network Attacks on State-of-the-Art Face Recognition — https://arxiv.org/abs/1801.00349
- Query Strategies for Evading Convex-Inducing Classifiers — https://people.eecs.berkeley.edu/~adj/publications/paper-files/1007-0484v1.pdf
- Adversarial Prompting for Black Box Foundation Models — https://arxiv.org/abs/2302.04237
- Automatically Evading Classifiers - A Case Study on PDF Malware Classifiers — http://evademl.org/docs/evademl.pdf
- Generic Black-Box End-to-End Attack against RNNs and Other API Calls Based Malware Classifiers — https://arxiv.org/abs/1707.05970
- GPTs Don't Keep Secrets - Searching for Backdoor Watermark Triggers in Autoregressive Language Models — https://aclanthology.org/2023.trustnlp-1.21/

**Envenenamiento (poisoning):**

- Instructions as Backdoors - Backdoor Vulnerabilities of Instruction Tuning for Large Language Models — https://arxiv.org/abs/2305.14710
- BadGPT - Exploring Security Vulnerabilities of ChatGPT via Backdoor Attacks to InstructGPT — https://arxiv.org/abs/2304.12298
- Towards Poisoning of Deep Learning Algorithms with Back-Gradient Optimization — https://arxiv.org/abs/1708.08689
- Efficient Label Contamination Attacks Against Black-Box Learning Models — https://www.ijcai.org/proceedings/2017/0551.pdf
- Text-to-Image Diffusion Models Can be Easily Backdoored through Multimodal Data Poisoning — https://arxiv.org/abs/2305.04175
- UOR - Universal Backdoor Attacks on Pre-Trained Language Models — https://arxiv.org/abs/2305.09574
- Analyzing And Editing Inner Mechanisms of Backdoored Language Models — http://arxiv.org/abs/2302.12461
- How to Backdoor Diffusion Models? — https://arxiv.org/abs/2212.05400
- On the Exploitability of Instruction Tuning — https://arxiv.org/abs/2306.17194
- Defending against Insertion-based Textual Backdoor Attacks via Attribution — https://aclanthology.org/2023.findings-acl.561/
- A Gradient Control Method for Backdoor Attacks on Parameter-Efficient Tuning — https://aclanthology.org/2023.acl-long.194/
- BadNL - Backdoor Attacks Against NLP Models with Semantic-Preserving Improvements — https://arxiv.org/abs/2006.01043
- Be Careful About Poisoned Word Embeddings — https://arxiv.org/abs/2103.15543
- BadPrompt - Backdoor Attacks on Continuous Prompts — https://arxiv.org/abs/2211.14719

**Privacidad:**

- Extracting Training Data from Diffusion Models — https://arxiv.org/abs/2301.13188
- Prompt Stealing Attacks Against Text-to-Image Generation Models — https://arxiv.org/abs/2305.13873
- Are Diffusion Models Vulnerable to Membership Inference Attacks? — https://arxiv.org/abs/2302.01316
- Model Inversion Attacks that Exploit Confidence Information and Basic Countermeasures — https://www.cs.cmu.edu/~mfredrik/papers/fjr2015ccs.pdf
- Multi-Step Jailbreaking Privacy Attacks on ChatGPT — http://arxiv.org/abs/2304.05197
- Flocks of Stochastic Parrots - Differentially Private Prompt Learning for Large Language Models — https://arxiv.org/abs/2305.15594
- ProPILE - Probing Privacy Leakage in Large Language Models — https://arxiv.org/abs/2307.01881
- Sentence Embedding Leaks More Information than You Expect — https://arxiv.org/pdf/2305.03010.pdf
- Text Embeddings Reveal (Almost) As Much As Text — https://arxiv.org/pdf/2310.06816.pdf
- Vec2Face - Unveil Human Faces from Their Blackbox Features in Face Recognition — https://arxiv.org/pdf/2003.06958.pdf
- Realistic Face Reconstruction from Deep Embeddings — https://openreview.net/pdf?id=-WsBmzWwPee

**Inyección:**

- DeepPayload - Black-box Backdoor Attack on Deep Learning Models through Neural Payload Injection — https://arxiv.org/abs/2101.06896
- Not What You've Signed Up For - Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection — https://arxiv.org/abs/2302.12173
- Latent Jailbreak - A Benchmark for Evaluating Text Safety and Output Robustness of Large Language Models — https://arxiv.org/abs/2307.08487
- Jailbreaker - Automated Jailbreak Across Multiple Large Language Model Chatbots — https://arxiv.org/abs/2307.08715
- (Ab)using Images and Sounds for Indirect Instruction Injection in Multi-Modal LLMs — https://arxiv.org/abs/2307.10490

**Redes/IDS (machine learning clásico):**

- Machine Learning Techniques for Intrusion Detection — https://arxiv.org/abs/1312.2177v2
- A Survey of Network Anomaly Detection Techniques — https://www.gta.ufrj.br/~alvarenga/files/CPE826/Ahmed2016-Survey.pdf
- Shallow and Deep Networks Intrusion Detection System - A Taxonomy and Survey — https://arxiv.org/abs/1701.02145v1
- A Taxonomy and Survey of Intrusion Detection System Design Techniques, Network Threats and Datasets — https://arxiv.org/pdf/1806.03517v1.pdf
- Next-Generation Intrusion Detection Systems — https://www.sciencedirect.com/science/article/abs/pii/S1574013716300153

**Endpoint / malware (clásico):**

- Deep Learning at the Shallow End - Malware Classification for Non-Domain Experts — https://arxiv.org/abs/1807.08265v1
- Malware Detection by Eating a Whole EXE — https://arxiv.org/pdf/1710.09435v1.pdf

**Aplicación web (clásico):**

- Adaptively Detecting Malicious Queries in Web Attacks — https://arxiv.org/pdf/1701.07774.pdf

**Comportamiento de usuario / fraude (clásico):**

- Detecting Anomalous User Behavior Using an Extended Isolation Forest Algorithm — https://arxiv.org/abs/1609.06676
- A Survey of Credit Card Fraud Detection Techniques — https://arxiv.org/abs/1611.06439v1
- Anomaly Detection in Industrial Control Systems Using CNNs — https://arxiv.org/abs/1806.08110v1

**Survey papers:**

- Deep Learning Algorithms for Cybersecurity Applications - A Technological and Status Review — https://www.sciencedirect.com/science/article/pii/S1574013720304172
- Machine Learning and Cybersecurity - Hype and Reality — https://cset.georgetown.edu/publication/machine-learning-and-cybersecurity/

**Modelos y datasets especializados (papers):**

- SecBench Paper — https://arxiv.org/abs/2412.20787
- NYU CTF Bench Paper — https://arxiv.org/abs/2406.05590
- SECURE Paper — https://arxiv.org/abs/2405.20441
- CyberMetric Paper — https://arxiv.org/abs/2402.07688
- SecLLMHolmes Paper — https://arxiv.org/abs/2312.12575v3
- LLM Offensive Security Benchmarking — https://arxiv.org/abs/2504.10112v1
- Ignore This Title and HackAPrompt (EMNLP'23) — https://arxiv.org/abs/2311.16119
- SelfCheckGPT — https://arxiv.org/abs/2303.08896

---

## 14. Libros y Publicaciones

- **AI for Cybersecurity by Cylance (2017)** — introducción a la IA para ciberseguridad. https://www.blackberry.com/us/en/forms/cylance/gated-content/introduction-to-ai-book
- **Machine Learning and Security** — aplicación del machine learning en seguridad. https://www.oreilly.com/library/view/machine-learning-and/9781491979891/
- **Mastering Machine Learning for Penetration Testing** — guía sobre el uso de machine learning para pentesting. https://www.packtpub.com/product/mastering-machine-learning-for-penetration-testing/9781788997409
- **Malware Data Science** — técnicas de data science para análisis de malware. https://nostarch.com/malwaredatascience
- **AI for Cybersecurity - A Handbook of Use Cases** — manual de casos de uso de IA en ciberseguridad. https://psucybersecuritylab.github.io/
- **Large Language Models in Cybersecurity: Threats, Exposure and Mitigation** (Springer, 2024) — guía de acceso abierto. https://link.springer.com/book/10.1007/978-3-031-54827-7
- **Generative AI Security: Theories and Practices** (Springer, 2024) — impactos de GenAI a través de la seguridad. https://link.springer.com/book/10.1007/978-3-031-54252-7
- **AI-Driven Cybersecurity and Threat Intelligence** (Springer, 2024) — IA por seguridad. https://link.springer.com/book/10.1007/978-3-031-15030-2
- **Developer's Playbook for LLM Security** (O'Reilly, 2024) — AppSec práctico de LLM. Steve Wilson. https://www.amazon.com/Developers-Playbook-Large-Language-Security/dp/109816220X

---

## 15. Cheatsheets y Guías

- **OWASP LLM Prompt Injection Prevention Cheat Sheet** — mejores prácticas de prevención. https://cheatsheetseries.owasp.org/cheatsheets/LLM_Prompt_Injection_Prevention_Cheat_Sheet.html
- **LangChain Security Policy** — "Four Perimeters" y endurecimiento de aplicaciones. https://python.langchain.com/docs/security/
- **CISA AI Security Best Practices** — guía de seguridad de sistemas de IA. https://www.cisa.gov/ai
- **NVIDIA AI Red Team Practical Advice** — hallazgos clave de evaluaciones AIRT. https://developer.nvidia.com/blog/practical-llm-security-advice-from-the-nvidia-ai-red-team/
- **Salesforce Prompt Injection Detection Guide** — construcción de sistemas de IA confiables. https://www.salesforce.com/blog/prompt-injection-detection/
- **OWASP Security Cheatsheets (general)** — serie de cheat sheets de OWASP para seguridad de aplicaciones. https://github.com/OWASP/CheatSheetSeries
- **MCP-Security-Checklist** — ver sección 2.4.
- **OffsecML Playbook** — colección integral de técnicas ofensivas y adversarias con demostraciones prácticas. https://wiki.offsecml.com

---

## 16. Certificaciones y Cursos

- **IBM Cybersecurity Analyst** (Coursera) — habilidades listas para el empleo en ciberseguridad. https://www.coursera.org/professional-certificates/ibm-cybersecurity-analyst
- **ISACA AAISM™** — AI Security Management (requiere CISM/CISSP). https://www.isaca.org/credentialing/aaism
- **ISC2 Building AI Strategy Certificate** — estrategia, gobernanza, riesgo. https://www.isc2.org/
- **Practical DevSecOps – CAISP (Certified AI Security Professional)** — certificación práctica con labs; 60 días de labs y defensas MITRE ATLAS. https://www.practical-devsecops.com/certified-ai-security-professional/
- **Securiti – AI Security & Governance** — gobernanza, privacidad, cumplimiento. https://education.securiti.ai/certifications/ai-governance/
- **SANS SEC545: GenAI & LLM AppSec** — seguridad GenAI práctica. https://www.sans.org/cyber-security-courses/genai-llm-application-security/
- **SANS SEC495: Building & Securing RAG** — entrenamiento de seguridad RAG. https://www.sans.org/cyber-security-courses/leveraging-llms-building-securing-rag/
- **SANS SEC411: AI Security Principles** — fundamentos con labs Docker. https://www.sans.org/cyber-security-courses/ai-security-principles-practices/
- **AppSecEngineer – AI Combat & Construct** — ataque/defensa de apps de IA. https://www.appsecengineer.com/
- **Practical AI Security Course (8kSec)** — ver sección 9.

---

## 17. Eventos y Conferencias

- **DEF CON (AI Village)** — challenges de red team de IA/GenAI. https://defcon.org/
- **Black Hat USA** — AI Security Summit y trainings. https://www.blackhat.com/
- **RSA Conference** — tracks de seguridad de IA, expo. https://www.rsaconference.com/
- **AI Risk Summit** (Ritz-Carlton, Half Moon Bay, CA) — ejecutivos de seguridad, investigadores de IA y policymakers discuten IA adversaria, deepfakes y desafíos regulatorios. https://airisksummit.com/
- **GCSCC AI Cybersecurity Conference** (Oxford, UK) — resiliencia cibernética en la era de la IA. https://gcscc.ox.ac.uk/
- **AI Security & Privacy Conference** — CISOs y ejecutivos C-Level con discusiones y casos de estudio. https://aisecurityconf.com/
- **Cyber-AI Conference** (Varna, Bulgaria) — avances de vanguardia en ciberseguridad e IA. https://cyber-ai.org/
- **AI Village** — comunidad, meetups y CTFs continuos. https://aivillage.org/
- **SANS AI Cybersecurity Summit** — workshops prácticos y demos en vivo de integración IA/ML en ciberseguridad. https://www.sans.org/cyber-security-summit/
- **HackAPrompt** — competencia de prompt hacking. https://www.hackaprompt.com/

---

## 18. Observabilidad y Monitoreo de LLMs

- **LangSmith** — tracing + evals para apps LLM. (LangChain) https://www.langchain.com/langsmith
- **Weights & Biases** — seguimiento de experimentos y gestión de prompts para LLMs. https://wandb.ai/
- **Langfuse** — tracing y monitoreo de costos open-source. https://langfuse.com/
- **Phoenix** — evaluación/monitoreo open-source. (Arize AI) https://phoenix.arize.com/
- **Helicone** — logging y analítica basados en proxy. https://www.helicone.ai/
- **Dynatrace Davis AI** — análisis de causa raíz impulsado por IA con baselining multidimensional y analítica predictiva. https://www.dynatrace.com/
- **LangKit** — ver sección 2.6.

---

## 19. Podcasts, YouTube, Blogs y Referentes

**Podcasts y newsletters:**

- **AI Security Podcast** (Ashish Rajan & Caleb Sima) — conversaciones vendor-neutral de seguridad de IA. https://www.aisecuritypodcast.com/
- **The AI Fix Podcast** (Graham Cluley & Mark Stockley) — deepfakes, política y seguridad. https://theaifix.show/
- **Smashing Security** (Graham Cluley & Carole Theriault) — pod semanal de infosec con temas de IA. https://www.smashingsecurity.com/
- **Resilient Cyber Newsletter** (Chris Hughes) — IA, supply chain, cloud, AppSec. https://www.resilientcyber.io/
- **MLSecOps podcast** — intersección de machine learning y operaciones de seguridad. https://mlsecops.com/podcast

**YouTube:**

- **John Hammond** — CTFs, tutoriales de hacking, resolución de problemas en tiempo real. https://www.youtube.com/@_JohnHammond
- **The Cyber Mentor** — ethical hacking práctico y pentesting. https://www.youtube.com/@TCMSecurityAcademy
- **NetworkChuck** — networking, ciberseguridad y tecnología. https://www.youtube.com/@NetworkChuck
- **Hak5** — herramientas de ciberseguridad, privacidad, gadgets. https://www.youtube.com/@hak5
- **MalwareTech** — análisis de malware en profundidad. https://www.youtube.com/@MalwareTechBlog
- **David Bombal** — ethical hacking, seguridad de red, certificaciones. https://www.youtube.com/@davidbombal
- **LiveOverflow** — explotación binaria, ingeniería inversa, CTF writeups. https://www.youtube.com/@LiveOverflow
- **CyberRisk TV** — cobertura de Black Hat 2025 con foco en seguridad de IA, IA agéntica y confianza. https://www.youtube.com/@CyberRiskTV
- **PowerDMARC** — autenticación de email, DMARC, spoofing, phishing. https://www.youtube.com/@PowerDMARC

**Blogs y otros recursos:**

- **Rez0's AI Security Blog** (Joseph Thacker) — fundamentos y técnicas de AI hacking. https://josephthacker.com/
- **Simon Willison's Blog** — prompt injection y seguridad de agentes. https://simonwillison.net
- **Lakera AI Blog** — liderazgo de pensamiento en seguridad GenAI. https://www.lakera.ai/blog
- **Anthropic Transparency Hub** — system cards y reportes de red team. https://www.anthropic.com/transparency
- **OpenAI Red Teaming Network** — documentación de red teaming e invitaciones. https://openai.com/index/red-teaming-network/
- **MLSecOps Community** — mejores prácticas y comunidad. https://mlsecops.com/
- **OWASP GenAI Security Project** — ver sección 1.
- **Lasso Security Blog** — recursos sobre ciberseguridad LLM/IA, seguridad MCP y red teaming. https://lasso.security/blog/

**Referentes / Thought Leaders:**

- **Simon Willison** — prompt injection y seguridad de agentes. https://twitter.com/simonw
- **Joseph Thacker (rez0)** — investigación prolífica de vulnerabilidades de IA. https://twitter.com/rez0__
- **Lakera Team** — creadores de Gandalf y Lakera Guard. https://twitter.com/lakeraai
- **NVIDIA AI Red Team** — equipo detrás de garak y guía de seguridad práctica. https://twitter.com/NVIDIAAIDev
- **Microsoft AI Red Team** — PyRIT y lecciones públicas de red teaming. https://twitter.com/MSFTSecurity
- **Steve Wilson** — líder del proyecto OWASP Top 10 para LLM Applications. https://www.linkedin.com/in/wilsonsd/
- **Ads Dawson** — líder técnico y de entradas de vulnerabilidad para OWASP Top 10 LLMs. https://www.linkedin.com/in/adamdawson0/

---

## 20. Otras Listas Awesome Relacionadas (IA + Seguridad)

- **awesome-llm-security** — recursos de seguridad LLM. (corca-ai) https://github.com/corca-ai/awesome-llm-security
- **awesome-gpt-security** — herramientas y casos de seguridad para apps GPT. (cckuailong) https://github.com/cckuailong/awesome-gpt-security
- **awesome-llm-cybersecurity-tools** — herramientas LLM para ciberseguridad. (Tenable, archivado) https://github.com/tenable/awesome-llm-cybersecurity-tools
- **Awesome-LLMSecOps** — ciclo de vida y amenazas de LLM SecOps. https://github.com/wearetyomsmnv/Awesome-LLMSecOps
- **awesome-llm-supply-chain-security** — recursos de seguridad de supply chain. https://github.com/ShenaoW/awesome-llm-supply-chain-security
- **awesome-MLSecOps** — herramientas y mejores prácticas de MLSecOps. https://github.com/RiccardoBiosas/awesome-MLSecOps
- **awesome-hallucination-detection** — papers de detección de alucinaciones. https://github.com/EdinburghNLP/awesome-hallucination-detection
- **oss-llm-security** — lista curada de herramientas de seguridad LLM open-source. https://github.com/kaplanlior/oss-llm-security
- **Awesome AI for Cybersecurity** — colección integral anterior, enfocada en aplicaciones de ML pre-LLM. https://github.com/Billy1900/Awesome-AI-for-cybersecurity
- **Awesome ML for Cybersecurity** — recurso establecido para enfoques ML tradicionales en seguridad. https://github.com/jivoi/awesome-ml-for-cybersecurity
- **Awesome AI Security (ottosulin)** — lista complementaria enfocada en seguridad de IA. https://github.com/ottosulin/awesome-ai-security
- **Awesome AI4DevSecOps** — integración reciente de tecnologías de IA en frameworks DevSecOps. https://github.com/awsm-research/Awesome-AI4DevSecOps
- **Awesome-MCP-Security (Puliczek)** — recurso definitivo cubriendo todos los aspectos de la seguridad de Model Context Protocol. https://github.com/Puliczek/awesome-mcp-security
- **awesome-cybersecurity-agentic-ai** — herramientas de ciberseguridad de IA agéntica y servidores MCP de seguridad. *(sin URL propia confirmada en la fuente original)*
- **awesome-ai-agents-security** — mapa enfocado de recursos de seguridad de agentes de IA. *(sin URL propia confirmada en la fuente original)*
- **Awesome-Offensive-AI-Agentic-Landscape** — panorama de agentes de IA ofensivos: agentes open-source, modelos especializados, papers, benchmarks y herramientas comerciales. *(sin URL propia confirmada en la fuente original)*
- **awesome-ai-agent-attacks** — línea de tiempo de incidentes reales de seguridad de agentes de IA. *(sin URL propia confirmada en la fuente original)*
- **AI Security Repository Radar** — radar de repositorios de seguridad IA/LLM/MCP/RAG actualizado diariamente. *(sin URL propia confirmada en la fuente original)*
- **awesome-ai-guardrails** — catálogo de modelos, herramientas, organizaciones, datasets y papers de guardrails de IA. *(sin URL propia confirmada en la fuente original)*
- **open-source-llm-scanners** — escáneres y herramientas de testing de LLM open-source. *(sin URL propia confirmada en la fuente original)*
- **awesome-ml-security (Trail of Bits)** — recursos curados de seguridad de machine learning. *(sin URL propia confirmada en la fuente original)*
- **awesome-ml-privacy-attacks** — papers de ataques de privacidad de machine learning. *(sin URL propia confirmada en la fuente original)*
- **awesome-ml-for-cybersecurity (clásica)** — lista clásica y grande de recursos de machine learning para ciberseguridad. https://github.com/jivoi/awesome-ml-for-cybersecurity
- **awesome-llm-security (general, corca-ai)** — asegurando LLMs. https://github.com/corca-ai/awesome-llm-security
- **awesome-threat-intelligence** — lista clásica de CTI. https://github.com/hslatman/awesome-threat-intelligence
- **awesome-threat-modelling** — metodologías y herramientas de threat modeling de propósito general (no IA). *(sin URL propia confirmada en la fuente original)*
- **Awesome-LLMs-for-Vulnerability-Detection** — índice enfocado y actualizado continuamente de investigación de detección de vulnerabilidades de software basada en LLM. *(sin URL propia confirmada en la fuente original)*
- **awesome-ai-cybersecurity-tools (scadastrangelove)** — la propia lista fusionada aquí para herramientas. https://github.com/scadastrangelove/awesome-ai-security-tools

---

## 21. Apéndice: Listas Generales de Hacking (no específicas de IA)

Estas listas fueron incluidas en la fuente `hack-with-github/awesome-hacking` (un directorio de listas "awesome" para hackers y pentesters). No son específicas de IA, pero se conservan aquí íntegramente porque formaban parte del material a fusionar y el usuario pidió no perder ningún enlace.

**Repositorios Awesome (por tema):**

| Tema | Enlace |
|---|---|
| Android Security | https://github.com/ashishb/android-security-awesome |
| AppSec | https://github.com/paragonie/awesome-appsec |
| Asset Discovery | https://github.com/redhuntlabs/Awesome-Asset-Discovery |
| Bug Bounty | https://github.com/djadmin/awesome-bug-bounty |
| Cellular Hacking | https://github.com/W00t3k/Awesome-Cellular-Hacking |
| CI/CD Attacks | https://github.com/TupleType/awesome-cicd-attacks |
| CTF | https://github.com/apsdehal/awesome-ctf |
| Cyber Security University | https://github.com/brootware/awesome-cyber-security-university |
| Cyber Skills | https://github.com/joe-shenouda/awesome-cyber-skills |
| Cybersources | https://github.com/bst04/CyberSources |
| Detection Engineering | https://github.com/infosecB/awesome-detection-engineering |
| DevSecOps | https://github.com/devsecops/awesome-devsecops |
| Drone Hacking | https://github.com/nicholasaleks/Awesome-Drone-Hacking |
| Embedded and IoT Security | https://github.com/fkie-cad/awesome-embedded-and-iot-security |
| Fuzzing | https://github.com/secfigo/Awesome-Fuzzing |
| Hacking (general) | https://github.com/carpedm20/awesome-hacking |
| Honeypots | https://github.com/paralax/awesome-honeypots |
| Incident Response | https://github.com/meirwah/awesome-incident-response |
| Industrial Control System Security | https://github.com/hslatman/awesome-industrial-control-system-security |
| InfoSec | https://github.com/onlurking/awesome-infosec |
| IoT and Hardware Security | https://github.com/kayranfatih/awesome-iot-and-hardware-security |
| Mainframe Hacking | https://github.com/samanL33T/Awesome-Mainframe-Hacking |
| Malware Analysis | https://github.com/rshipp/awesome-malware-analysis |
| Malware Persistence | https://github.com/Karneades/awesome-malware-persistence |
| Node.js Security | https://github.com/lirantal/awesome-nodejs-security |
| OSINT | https://github.com/jivoi/awesome-osint |
| OSX and iOS Security | https://github.com/ashishb/osx-and-ios-security-awesome |
| Password Cracking | https://github.com/n0kovo/awesome-password-cracking |
| Pcaptools | https://github.com/caesar0301/awesome-pcaptools |
| Pentest | https://github.com/enaqx/awesome-pentest |
| PHP Security | https://github.com/ziadoz/awesome-php#security |
| Prompt Injection | https://github.com/Joe-B-Security/awesome-prompt-injection |
| Real-time Communications Hacking (VoIP/WebRTC/VoLTE) | https://github.com/EnableSecurity/awesome-rtc-hacking |
| Red Teaming Toolkit | https://github.com/infosecn1nja/Red-Teaming-Toolkit |
| Reinforcement Learning for Cyber Security | https://github.com/Kim-Hammar/awesome-rl-for-cybersecurity |
| Reversing | https://github.com/HACKE-RC/awesome-reversing |
| Sec Talks | https://github.com/PaulSec/awesome-sec-talks |
| SecLists | https://github.com/danielmiessler/SecLists |
| Security (general) | https://github.com/sbilly/awesome-security |
| Social Engineering | https://github.com/giuliacassara/awesome-social-engineering |
| Static Analysis | https://github.com/analysis-tools-dev/static-analysis |
| The Art of Hacking Series | https://github.com/The-Art-of-Hacking/h4cker |
| Threat Intelligence | https://github.com/hslatman/awesome-threat-intelligence |
| Vehicle Security | https://github.com/jaredthecoder/awesome-vehicle-security |
| Web Hacking | https://github.com/infoslack/awesome-web-hacking |
| Web3 Security | https://github.com/Anugrahsr/Awesome-web3-Security |
| YARA | https://github.com/InQuest/awesome-yara |

**Otros repositorios útiles:**

| Recurso | Enlace |
|---|---|
| AI Security (DeepSpaceHarbor) | https://github.com/DeepSpaceHarbor/Awesome-AI-Security |
| Annual Security Reports | https://github.com/jacobdjwilson/awesome-annual-security-reports |
| API Security Checklist | https://github.com/shieldfy/API-Security-Checklist |
| APT Notes | https://github.com/kbandla/APTnotes |
| Bug Bounty Reference | https://github.com/ngalongc/bug-bounty-reference |
| Capsulecorp Pentest | https://github.com/r3dy/capsulecorp-pentest |
| Cryptography | https://github.com/sobolevn/awesome-cryptography |
| CVE PoC | https://github.com/trickest/cve |
| CyberChef | https://gchq.github.io/CyberChef/ |
| Detection Lab | https://github.com/clong/DetectionLab |
| Executable Packing | https://github.com/packing-box/awesome-executable-packing |
| Forensics | https://github.com/Cugu/awesome-forensics |
| Free Programming Books | https://github.com/EbookFoundation/free-programming-books |
| GTFOBins | https://gtfobins.github.io |
| Hacker101 | https://github.com/Hacker0x01/hacker101 |
| Infosec Getting Started | https://github.com/gradiuscypher/infosec_getting_started |
| Infosec Reference | https://github.com/rmusser01/Infosec_Reference |
| IOC | https://github.com/sroberts/awesome-iocs |
| Linux Kernel Exploitation | https://github.com/xairy/linux-kernel-exploitation |
| Machine Learning for Cyber Security | https://github.com/jivoi/awesome-ml-for-cybersecurity |
| Payloads | https://github.com/foospidy/payloads |
| PayloadsAllTheThings | https://github.com/swisskyrepo/PayloadsAllTheThings |
| Pentest Wiki | https://github.com/nixawk/pentest-wiki |
| Probable Wordlists | https://github.com/berzerk0/Probable-Wordlists |
| Red Team Physical Tools | https://github.com/DavidProbinsky/RedTeam-Physical-Tools |
| Reverse Engineering (reading list) | https://github.com/onethawt/reverseengineering-reading-list |
| RFSec-ToolKit | https://github.com/cn0xroot/RFSec-ToolKit |
| Security Cheatsheets (OWASP) | https://github.com/OWASP/CheatSheetSeries |
| Shell | https://github.com/alebcay/awesome-shell |
| Suricata | https://github.com/satta/awesome-suricata |
| ThreatHunter-Playbook | https://github.com/OTRF/ThreatHunter-Playbook |
| Tor | https://github.com/polycarbohydrate/awesome-tor |
| Vulhub | https://github.com/vulhub/vulhub |
| Web Security | https://github.com/qazbnm456/awesome-web-security |

---

