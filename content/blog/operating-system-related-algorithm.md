---
title: Operating System Related Algorithm
date: 2025-12-29T12:41:37.025Z
---

# 🖥️ Operating System (OS) Concepts

---

## ⚙️ CPU Scheduling Algorithms
- 🕰️ **FCFS (First Come First Serve)** — simple, may cause long waiting
- ⏱️ **SJF (Shortest Job First)** — minimum average waiting time
- 🔁 **SRTF (Shortest Remaining Time First)** — preemptive SJF
- 🔄 **RR (Round Robin)** — time-sliced, fair for all processes
- 🧩 **MLQ (Multilevel Queue)** — multiple queues with priorities

---

## 🧠 Memory Management
- 📄 **Paging** — fixed-size pages, no external fragmentation
- 🧱 **Segmentation** — logical division (code, stack, data)
- 🌐 **Virtual Memory** — illusion of large memory using disk

### 🔁 Page Replacement Algorithms
- 🥇 **FIFO** — first loaded page removed (Belady’s anomaly ❌)
- 🧠 **LRU** — removes least recently used page
- 🎯 **Optimal** — replaces page used farthest in future (theoretical)

---

## 📁 File Allocation Methods
- 📦 **Contiguous Allocation** — fast access, fragmentation issue
- 🔗 **Linked Allocation** — no fragmentation, slow access
- 🗂️ **Indexed Allocation** — uses index block, balanced approach

---

## 💽 Disk Scheduling Algorithms
- 🕰️ **FCFS** — simple, inefficient head movement
- 🎯 **SSTF** — shortest seek time first
- 🛗 **SCAN (Elevator)** — moves back and forth
- 🔄 **C-SCAN** — circular scan, uniform waiting
- 👀 **LOOK** — scan only till last request
- 🔁 **C-LOOK** — circular version of LOOK

---

## 🔒 Deadlock Handling
- 🚫 **Deadlock Prevention** — eliminate conditions
- 🛡️ **Deadlock Avoidance** — safe state checking
- 🏦 **Banker’s Algorithm** — resource safety algorithm
- 🕸️ **Resource Allocation Graph (RAG)** — detect deadlocks visually
