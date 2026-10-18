# 🚕 Distributed Multi-Agent Taxi Di## 📋 Table of Contents
- [✨ Key Features](#-key-features)
- [🏗️ System Architecture](#️-system-architecture)
- [💻 Technology Stack](#-technology-stack)
- [📦 Installation](#-installation)
- [⚙️ Configuration](#️-configuration)
- [🚀 Usage](#-usage)
- [🧪 Performance Evaluation](#-performance-evaluation)
- [🌐 Multi-Host Distribution](#-multi-host-distribution)
- [📚 Project Documentation](#-project-documentation)
- [🛠️ Development](#️-development)
- [📊 Project Statistics](#-project-statistics)

## 📚 Quick Links

- 🚀 **[Quick Start Guide](QUICKSTART.md)** - Get running in 10 minutes
- 🛠️ **[Development Guide](DEVELOPMENT.md)** - For developers and contributors
- 📖 **[API Documentation](docs/API.md)** - Technical API reference
- 🧪 **[Performance Tests](docs/PERFORMANCE.md)** - Benchmarking and evaluation

## 💻 Technology Stack
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![SPADE](https://img.shields.io/badge/SPADE-3.2+-green.svg)](https://spade-mas.readthedocs.io/)
[![OR-Tools](https://img.shields.io/badge/OR--Tools-9.5+-orange.svg)](https://developers.google.com/optimization)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **Final Project - Tópicos de Ciencias de la Computación 2025-1**  
> **Universidad Peruana de Ciencias Aplicadas**

A sophisticated **distributed multi-agent system** for intelligent taxi dispatching using **constraint programming** and **optimization** with **OR-Tools**. Built with the **SPADE framework** for scalable agent communication and deployment across multiple hosts.

## ✨ Key Features

### 🎯 **Core Capabilities**
- ✅ **Distributed Multi-Agent Architecture** using SPADE framework
- ✅ **Constraint Programming Optimization** with Google OR-Tools CP-SAT solver
- ✅ **Horizontal Scalability** across multiple hosts and networks
- ✅ **Real-time GUI Dashboard** with live statistics and visualization
- ✅ **Fault Tolerance** with automatic reconnection and error recovery
- ✅ **Performance Evaluation Suite** with automated limit testing

### 🤖 **Intelligent Agents**
- **TaxiAgent**: Autonomous taxi entities with independent decision-making
- **CoordinatorAgent**: Central optimization engine managing global assignments
- **XMPP Communication**: Robust messaging protocol via Openfire server
- **Dynamic User Management**: Automatic creation and cleanup of XMPP users

### 🧮 **Advanced Optimization**
- **Constraint Programming**: Optimal taxi-passenger assignments
- **Operational Constraints**: Maximum distance (15 cells), capacity (4 passengers)
- **Objective Function**: Minimization of passenger waiting times
- **Real-time Solving**: Reassignments every 2 seconds with sub-100ms response

## 🏗️ System Architecture

## 📋 Table of Contents

- [✨ Key Features](#-key-features)
- [🏗️ System Architecture](#️-system-architecture)
- [💻 Technology Stack](#-technology-stack)
- [📦 Installation](#-installation)
- [⚙️ Configuration](#️-configuration)
- [🚀 Usage](#-usage)
- [🧪 Performance Evaluation](#-performance-evaluation)
- [🌐 Multi-Host Distribution](#-multi-host-distribution)
- [📚 Project Documentation](#-project-documentation)
- [🛠️ Development](#️-development)
- [📊 Project Statistics](#-project-statistics)

## � Technology Stack

| Technology | Version | Purpose |
|------------|---------|---------|
| **Python** | 3.8+ | Primary development language |
| **SPADE** | 3.2+ | Multi-agent system framework |
| **OR-Tools** | 9.5+ | Constraint programming solver |
| **Openfire** | 4.7+ | XMPP server for agent communication |
| **Tkinter** | Built-in | Graphical user interface |
| **Requests** | 2.28+ | REST API client |
| **PSUtil** | 5.9+ | System monitoring |

## 📦 Installation

```
┌─────────────────────────────────────────────────────────────┐
│                    Distributed System                      │
├─────────────────────┬─────────────────────┬─────────────────┤
│     Host 1          │     Host 2          │     Host N      │
│  ┌─────────────┐    │  ┌─────────────┐    │  ┌─────────────┐│
│  │ TaxiAgent 1 │    │  │ TaxiAgent N │    │  │ TaxiAgent X ││
│  │ TaxiAgent 2 │    │  │ TaxiAgent N+1│   │  │ TaxiAgent Y ││
│  │     ...     │    │  │     ...     │    │  │     ...     ││
│  └─────────────┘    │  └─────────────┘    │  └─────────────┘│
└─────────────────────┴─────────────────────┴─────────────────┘
                              │
                    ┌─────────────────────┐
                    │   Openfire Server   │
                    │    (XMPP/REST)      │
                    └─────────────────────┘
                              │
                    ┌─────────────────────┐
                    │  CoordinatorAgent   │
                    │   + OR-Tools CPSat  │
                    │   + GUI Dashboard   │
                    └─────────────────────┘
```

### Core Components

#### 🚗 **Distributed Intelligent Agents (TaxiAgent)**
TaxiAgents form the operational foundation of the system, where each taxi is modeled as an autonomous entity with:
- **Autonomous state management**: Position, capacity, availability
- **Local decision making**: Independent routing and behavior
- **Asynchronous communication**: Status reporting to coordinator
- **Distributed scalability**: Execution across multiple hosts

#### 🎮 **Central Coordinator Agent (CoordinatorAgent)**
The CoordinatorAgent acts as the system's brain, managing:
- **Global information**: State of all taxis and passengers
- **Decision processing**: Assignments using constraint programming
- **Graphical interface**: Real-time system visualization
- **Performance metrics**: Monitoring and reporting

#### 🔧 **Constraint Programming Module**
Specialized optimization system based on OR-Tools:
- **Constraint modeling**: Maximum distance (15 cells), capacity (4 passengers)
- **Objective function**: Minimization of waiting time with penalties
- **CP-SAT Solver**: Optimal real-time resolution
- **Dynamic reassignments**: Every 2 seconds based on conditions

#### 📡 **Multi-Agent Communication System**
Distributed communication architecture with:
- **SPADE Framework**: Agent development in Python
- **XMPP Protocol**: Robust communication via Openfire
- **Automatic management**: REST API for XMPP users
- **Fault tolerance**: Automatic reconnection

### Prerequisites

1. **Python 3.8 or higher**
2. **Java 8+ (for Openfire)**
3. **Git**

### Step 1: Clone Repository

```bash
git clone https://github.com/your-username/taxi-dispatch-multiagent.git
cd taxi-dispatch-multiagent
```

### Step 2: Create Virtual Environment

```bash
python -m venv venv

# Windows
venv\Scripts\activate

# Linux/Mac
source venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Setup Openfire Server

#### Installation

```bash
# Windows: Download from https://www.igniterealtime.org/downloads/
# Linux Ubuntu/Debian:
wget https://www.igniterealtime.org/downloadServlet?filename=openfire/openfire_4_7_4.tar.gz
tar -xzf openfire_4_7_4.tar.gz
```

#### Initial Configuration

1. **Start Openfire**:
   ```bash
   # Windows: Run openfire.exe as administrator
   # Linux:
   cd openfire/bin
   ./openfire start
   ```

2. **Configure via Web Console**:
   - Navigate to: `http://localhost:9090`
   - Follow setup wizard
   - **Domain**: `localhost`
   - **Admin**: User `admin`, Password `123`

3. **Install REST API Plugin**:
   - `Plugins` > `Available Plugins` > `REST API`
   - Install and configure secret token

## ⚙️ Configuration

### Main Configuration File: `src/config.py`

```python
@dataclass 
class TaxiSystemConfig:
    # OpenFire/XMPP Configuration
    openfire_host: str = "localhost"
    openfire_port: int = 9090
    openfire_admin_user: str = "admin"
    openfire_admin_password: str = "123"
    openfire_domain: str = "localhost"
    
    # Grid Configuration
    grid_width: int = 30
    grid_height: int = 30
    
    # System Parameters
    num_taxis: int = 3
    initial_passengers: int = 4
    taxi_capacity: int = 4
    
    # Timing
    assignment_interval: float = 2.0
    taxi_speed: float = 1.0
    
    # Constraints
    max_pickup_distance: int = 15
    wait_penalty_factor: float = 2.0
```

### REST API Authentication Token

Configure in `src/services/openfire_api.py`:

```python
self.headers = {
    "Authorization": "YOUR_SECRET_TOKEN_HERE"
}
```

> 💡 **Tip**: The token can be found in Openfire console: `Server` > `Server Settings` > `REST API` > `Secret key`

## 🚀 Usage

### GUI Mode (Recommended)

```bash
python main.py
```

**GUI Features**:
- 📊 **Statistics Panel**: Active taxis, passengers, solver status
- 🎮 **Controls**: Start, stop, restart system
- 🗺️ **Interactive Map**: Real-time visualization of 30x30 grid
- 📋 **Legend**: Symbols for taxis, passengers, destinations

### Command Line Mode

#### Create Taxi Agents

```bash
# Local host: Create 5 taxis
python main.py --host taxi_host --agent-type taxi --agent-count 5

# Coordinator host
python main.py --host coordinator_host --agent-type coordinator
```

#### Multi-Host Distribution

```bash
# Host 1: 10 taxis
python main.py --host host1 --agent-type taxi --agent-count 10

# Host 2: 15 taxis
python main.py --host host2 --agent-type taxi --agent-count 15

# Main host: Coordinator with GUI
python main.py --host coordinator --agent-type coordinator
```

### Command Line Parameters

| Parameter | Description | Example |
|-----------|-------------|---------|
| `--host` | Host identifier | `--host server1` |
| `--agent-type` | Agent type | `--agent-type taxi` |
| `--agent-count` | Number of agents | `--agent-count 20` |

## 🧪 Performance Evaluation

### Included Testing Scripts

#### 1. **Multi-Host Limit Evaluation**

```bash
python comparador_limite_multi_host.py
```

**Features**:
- Automated testing with 2 and 3 hosts
- RAM usage monitoring during creation
- Limit detection when RAM > 90%
- JSON report with memory flags

#### 2. **Quick Performance Test**

```bash
python quick_performance_test.py
```

#### 3. **Distributed Evaluation**

```bash
python evaluacion_multi_host.py
```

#### 4. **User Management**

```bash
# Clean Openfire users
python deleteagents.py

# Connection diagnostics
python test_openfire_connection.py
```

### Evaluated Metrics

- ✅ **Maximum agents per host**
- ✅ **RAM usage** during operation
- ✅ **System response time**
- ✅ **XMPP communication latency**
- ✅ **Assignment success rate**

### Typical Results

| Metric | Typical Value |
|---------|--------------|
| **Agents per host** | 50-100+ |
| **Assignment time** | <100ms |
| **RAM usage** | ~50MB per agent |
| **XMPP latency** | <10ms |

## 🌐 Multi-Host Distribution

### Network Configuration

1. **Central Openfire Server**:
   ```bash
   # Configure firewall for ports
   # 5222: XMPP
   # 9090: Web console
   # 9091: REST API
   ```

2. **Remote Hosts**:
   ```python
   # Modify config.py on each host
   openfire_host = "192.168.1.100"  # Central server IP
   ```

### Distributed Deployment Example

```bash
# Central Server (192.168.1.100)
python main.py --host coordinator --agent-type coordinator

# Host 1 (192.168.1.101)
python main.py --host host1 --agent-type taxi --agent-count 25

# Host 2 (192.168.1.102)
python main.py --host host2 --agent-type taxi --agent-count 30

# Host 3 (192.168.1.103)
python main.py --host host3 --agent-type taxi --agent-count 35
```

### Multi-Host Evaluation Script

```bash
# Evaluate distributed limits
python comparador_limite_multi_host.py --hosts 3 --start-agents 10

# Expected output:
# - 2-host configuration: X maximum agents
# - 3-host configuration: Y maximum agents
# - Detailed JSON report
```

## 📚 Project Documentation

### Project Structure

```
tfsito/
├── src/
│   ├── agent/
│   │   ├── coordinator.py      # Central coordinator agent
│   │   ├── taxi.py            # Individual taxi agent
│   │   ├── index.py           # Agent factory
│   │   └── libs/
│   │       ├── constraint.py   # Constraint programming
│   │       └── environment.py  # Environment structures
│   ├── services/
│   │   └── openfire_api.py    # Openfire REST API client
│   ├── utils/
│   │   └── logger.py          # Logging system
│   ├── config.py              # Global configuration
│   └── taxi_dispatch_gui.py   # Graphical interface
├── main.py                    # Main entry point
├── deleteagents.py           # Cleanup utility
├── comparador_limite_multi_host.py  # Limit evaluation
├── test_openfire_connection.py      # Diagnostics
└── requirements.txt          # Dependencies
```

### Openfire REST API

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/plugins/restapi/v1/users` | GET | List users |
| `/plugins/restapi/v1/users` | POST | Create user |
| `/plugins/restapi/v1/users/{id}` | DELETE | Delete user |
| `/plugins/restapi/v1/sessions` | GET | Active sessions |
