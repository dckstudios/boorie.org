# Boorie - Agente IA para Ingeniería Hidráulica 💧

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python](https://img.shields.io/badge/python-3.8%20%7C%203.9%20%7C%203.10%20%7C%203.11-blue)](https://www.python.org)
[![Status](https://img.shields.io/badge/Status-Pre--Alpha-orange)](https://github.com/boorie/boorie)
[![Community](https://img.shields.io/badge/Community-Discord-7289da)](https://discord.gg/boorie)
[![Documentation](https://img.shields.io/badge/docs-latest-brightgreen)](https://docs.boorie.org)

[English](#english) | [Español](#español)

---

## Español

### 🌊 Acerca de Boorie

Boorie es un agente de inteligencia artificial especializado en ingeniería hidráulica que integra WNTR (Water Network Tool for Resilience) con modelos de lenguaje avanzados (LLMs) para asistir a ingenieros en la gestión y optimización de redes de agua urbanas.

### 🎯 Misión

Democratizar el acceso a herramientas avanzadas de análisis hidráulico mediante IA, permitiendo a ingenieros de todo el mundo optimizar la gestión del agua urbana de manera más eficiente y sostenible.

### ✨ Características Principales

- **🧠 Análisis Contextual**: Comprende en qué etapa del proyecto te encuentras
- **🔧 Integración WNTR**: Análisis hidráulico completo y simulaciones
- **🤖 Multi-LLM**: Compatible con modelos open source y propietarios vía LiteLLM
- **📚 Base de Conocimiento**: RAG especializado en normativas y mejores prácticas hidráulicas
- **🌐 API REST**: Desplegable con FastAPI para integraciones empresariales
- **👥 Colaborativo**: Diseñado para trabajo en equipo con trazabilidad completa

### 🚀 Inicio Rápido

```bash
# Crear entorno virtual
python -m venv env
source env/bin/activate  # En macOS/Linux
# o
env\Scripts\activate  # En Windows

# Instalar Boorie
pip install boorie

# Ejecutar ejemplo básico
boorie analyze network.inp --stage preliminary
```

### 📋 Requisitos

- Python 3.8 - 3.11
- WNTR >= 0.5.0
- LiteLLM >= 1.0.0
- FastAPI >= 0.100.0 (para despliegue API)

### 🏗️ Arquitectura del Proyecto

```
boorie/
├── boorie/              # Código fuente principal
│   ├── core/           # Núcleo del agente IA
│   ├── agents/         # Agentes especializados por etapa
│   ├── tools/          # Herramientas hidráulicas
│   └── api/            # API REST
├── docs/               # Documentación técnica
├── rag-knowledge/      # Base de conocimiento para RAG
├── community-site/     # Sitio web de la comunidad
├── examples/           # Ejemplos de uso
└── tests/             # Suite de pruebas
```

### 🤝 Socios del Proyecto

#### Socios Fundadores
- **[Isla Creativa](https://islacreativa.com)** - Desarrollo principal y mantenimiento
- **[Universidad XYZ]** - Investigación y validación académica
- **[Empresa Agua ABC]** - Casos de uso industriales y pruebas piloto

#### Colaboradores Estratégicos
- **[Fundación Agua Limpia]** - Implementación en comunidades vulnerables
- **[Instituto Nacional del Agua]** - Normativas y estándares

### 🌍 Comunidad

#### Canales de Comunicación
- **[Discord](https://discord.gg/boorie)** - Chat en tiempo real
- **[Foro](https://forum.boorie.org)** - Discusiones técnicas
- **[Blog](https://blog.boorie.org)** - Actualizaciones y casos de éxito

#### Cómo Contribuir
Lee nuestro [CONTRIBUTING.md](CONTRIBUTING.md) para conocer cómo puedes ayudar.

### 📊 Hoja de Ruta

#### Q1 2024 - Fundación
- [x] Arquitectura base del agente
- [x] Integración WNTR básica
- [ ] Primera versión alpha pública
- [ ] Documentación inicial

#### Q2 2024 - Expansión
- [ ] RAG con normativas hidráulicas
- [ ] Soporte multi-idioma completo
- [ ] Herramientas de visualización
- [ ] API v1.0 estable

#### Q3 2024 - Producción
- [ ] Interfaz web completa
- [ ] Integraciones empresariales
- [ ] Certificación ISO
- [ ] Programa de formación

### 📄 Licencia

Este proyecto está licenciado bajo Apache License 2.0 - ver [LICENSE](LICENSE) para más detalles.

### 🆘 Soporte

- **Documentación**: [docs.boorie.org](https://docs.boorie.org)
- **Issues**: [GitHub Issues](https://github.com/boorie/boorie/issues)
- **Email**: support@boorie.org
- **Empresarial**: enterprise@boorie.org

---

## English

### 🌊 About Boorie

Boorie is an AI-powered hydraulic engineering agent that integrates WNTR (Water Network Tool for Resilience) with advanced language models (LLMs) to assist engineers in managing and optimizing urban water networks.

### 🎯 Mission

To democratize access to advanced hydraulic analysis tools through AI, enabling engineers worldwide to optimize urban water management more efficiently and sustainably.

### ✨ Key Features

- **🧠 Contextual Analysis**: Understands your project stage
- **🔧 WNTR Integration**: Complete hydraulic analysis and simulations
- **🤖 Multi-LLM**: Compatible with open source and proprietary models via LiteLLM
- **📚 Knowledge Base**: RAG specialized in hydraulic regulations and best practices
- **🌐 REST API**: Deployable with FastAPI for enterprise integrations
- **👥 Collaborative**: Designed for teamwork with complete traceability

### 🚀 Quick Start

```bash
# Create virtual environment
python -m venv env
source env/bin/activate  # On macOS/Linux
# or
env\Scripts\activate  # On Windows

# Install Boorie
pip install boorie

# Run basic example
boorie analyze network.inp --stage preliminary
```

### 📋 Requirements

- Python 3.8 - 3.11
- WNTR >= 0.5.0
- LiteLLM >= 1.0.0
- FastAPI >= 0.100.0 (for API deployment)

### 🏗️ Project Architecture

```
boorie/
├── boorie/              # Main source code
│   ├── core/           # AI agent core
│   ├── agents/         # Stage-specific agents
│   ├── tools/          # Hydraulic tools
│   └── api/            # REST API
├── docs/               # Technical documentation
├── rag-knowledge/      # Knowledge base for RAG
├── community-site/     # Community website
├── examples/           # Usage examples
└── tests/             # Test suite
```

### 🤝 Project Partners

#### Founding Partners
- **[Isla Creativa](https://islacreativa.com)** - Main development and maintenance
- **[University XYZ]** - Academic research and validation
- **[Water Company ABC]** - Industrial use cases and pilot testing

#### Strategic Collaborators
- **[Clean Water Foundation]** - Implementation in vulnerable communities
- **[National Water Institute]** - Regulations and standards

### 🌍 Community

#### Communication Channels
- **[Discord](https://discord.gg/boorie)** - Real-time chat
- **[Forum](https://forum.boorie.org)** - Technical discussions
- **[Blog](https://blog.boorie.org)** - Updates and success stories

#### How to Contribute
Read our [CONTRIBUTING.md](CONTRIBUTING.md) to learn how you can help.

### 📊 Roadmap

#### Q1 2024 - Foundation
- [x] Base agent architecture
- [x] Basic WNTR integration
- [ ] First public alpha version
- [ ] Initial documentation

#### Q2 2024 - Expansion
- [ ] RAG with hydraulic regulations
- [ ] Complete multi-language support
- [ ] Visualization tools
- [ ] Stable API v1.0

#### Q3 2024 - Production
- [ ] Complete web interface
- [ ] Enterprise integrations
- [ ] ISO certification
- [ ] Training program

### 📄 License

This project is licensed under Apache License 2.0 - see [LICENSE](LICENSE) for more details.

### 🆘 Support

- **Documentation**: [docs.boorie.org](https://docs.boorie.org)
- **Issues**: [GitHub Issues](https://github.com/boorie/boorie/issues)
- **Email**: support@boorie.org
- **Enterprise**: enterprise@boorie.org

---

<div align="center">
  <sub>Built with ❤️ by the Boorie Community</sub>
</div>