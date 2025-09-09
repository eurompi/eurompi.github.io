---
permalink: program
---

<script type="text/javascript" src="/assets/js/timeconvert.js"></script>

![Banner](/assets/Charlotte1.png){:height="auto" width="100%"}

# EuroMPI/USA'25 Program

The program below is tentative and might change. The EuroMPI program runs in parallel with the [IWOMP program](https://www.iwomp.org/iwomp-2025/).

## Oct 1 - Day 1

[gropp]: ## "The MPI standard was created 31 years ago. During that time, the MPICH implementation of MPI has both provided users with a high-performance yet portable implementation and has contributed to the evolution of the MPI standard. In recognition of its impact, ACM recognized MPICH with the 2024 Software System Award. In this talk I will review how MPICH came to be, features and decisions that contributed to its success, and some comments on both the future of MPICH and MPI."

[oraji]:## "Parallel programming models such as MPI and OpenSHMEM enable the use of large-scale distributed-memory computers in HPC. However, programmers often miss subtle rules regarding their APIs, such as properly synchronizing local memory accesses with communication and releasing acquired resources. Existing correctness tools aim to detect these issues automatically, but are typically model-specific. We propose the use of model-independent function annotations to avoid this dependency:
Contracts allow the specification of generic pre- and postconditions at function declarations. We specify requirements that must be satisfied at the corresponding call sites to avoid common MPI errors such as resource leaks and local data races. The transparent nature of contracts also allows for easier maintainability and extensibility of checks. This paper presents a contract language and CoVer, an extensible static verifier to check the use of library-based parallel programming models. It applies data-flow analysis using the LLVM framework to verify these contract annotations. We compare detection accuracy against the static tools PARCOACH and MPI-Checker using RMARaceBench and MPI-BugBench, and compile-time overhead based on the mini-apps LULESH, miniVite, and the PRK Stencil Kernel. CoVer improved the detection accuracy by covering a wide variety of issues, while maintaining comparable overhead."

[optenhoefel]:## "Non-blocking communication in MPI significantly enhances high-performance computing by minimizing communication overhead through the overlap of computation and communication. Asynchronous programming models further enhance efficiency and adaptability in load balancing; however, the integration of MPI communication with these models remains insufficient.
The MPI Continuations proposal, currently under discussion in the MPI Forum, aims to resolve this by introducing asynchronous completion for non-blocking communication. To ensure application developers can adopt this transformative feature, robust support in PMPI-based tools is essential.
&nbsp;
We have updated an early prototype to align with the latest discussions from the MPI Forum. This shim library is compatible with any MPI implementation. We describe potential pitfalls in implementing continuations, including a significant API issue that could lead to race conditions. We propose restrictions to prevent these issues and strengthen the robustness of the MPI Continuations proposal.
&nbsp;
Additionally, our analysis highlights the challenges PMPI-based tools will face with the new control flow, as MPI operations may now complete at nearly any point in a program. Progress engines might also become visible, requiring closer attention. Tools need to adapt by intercepting user-provided callback functions to effectively monitor the completion of non-blocking communication. Our extended PMPI-based On-the-Fly Critical Path Tool (OTF-CPT) demonstrates a clear path for integrating MPI Continuations into performance analysis tools, enhancing overall performance and adaptability in advanced computing applications."

[burak]:## "Modern multi-node systems necessitate parallel programming models (PPMs) like MPI to facilitate execution and communication among multiple processing elements. These SPMD PPMs offer features such as RMA or accelerator support. However, SPMD program tools, such as those for correctness checks or performance optimization, are typically developed for specific PPMs or rely on tool-internal abstractions. To overcome this limitation, SPMD IR was introduced as an intermediate representation (IR) within a multi-layer program representation and realized as a dialect in MLIR (LLVM).
&nbsp;
This work extends the SPMD IR by incorporating, among others, capabilities for RMA and related synchronization mechanisms. These enhancements increase compatibility with MPI and SHMEM, while newly integrating support for NVSHMEM. By leveraging traits in MLIR, SPMD IR provides an extensible approach for implementing SPMD program analysis.
&nbsp;
The applicability of the SPMD IR is demonstrated through the use case of static local data race detection. It is implemented in a generalized fashion, covering not only RMA but also non-blocking communication in general, and is independent of specific API calls, offering increased extensibility. Using a comprehensive set of micro-benchmark suites and proxy apps, the SPMD IR is evaluated against both static and dynamic tools. Overall, the SPMD IR verification distinguishes itself with extensive PPM support and high detection accuracy. Notably, it is the first tool capable of detecting data races across SHMEM, NVSHMEM, and their hybrid combinations (with MPI)."

[li]:## "The increasing disparity between computing capabilities and communication bandwidth has become a major bottleneck in High Performance Computing (HPC) applications. To address this challenge, we introduce a framework that leverages early data compression for communication data within the Open MPI library with the use of userfaultfd (uffd) for efficient write detection. By integrating the high-speed LZ4 compression algorithm, the proposed framework minimizes communication overhead by reducing the size of data transmitted among processes while hiding compression overhead behind either pack or communication overhead. Applying our uffd framework onto Livermore Unstructured Lagrangian Explicit Shock Hydrodynamics (LULESH) highlights the potential of the framework in reducing data communication volumes and overall communication latency, paving the way for improved performance in HPC environments."

| Start | End   | Session |
|-------|-------|---------|
| 8:30  | 9:00  | Registration & Coffee |
| **9:00**  | **10:00**  | Tutorial, Part I: General Overview of MPI |
| 10:00 | 10:30 | Coffee Break |
| 10:30 | 11:00 | Tutorial, Part II: Current Topics in MPI |
| 11:00 | 11:30 |  |
| 11:30 | 12:00 |  |
| 12:00 | 13:30 | Lunch Break |
| 13:30 | 14:00 | **Joint Keynote I - Amanda Randles (Duke University)** |
| 14:00 | 14:30 |  |
| 14:30 | 15:00 | Coffee Break |
| **15:30** | **17:00** | **Session I: Correctness** |
| 15:30 | 16:00 | [**Verifying MPI API Usage Requirements with Contracts.**][oraji] (Yussur Mustafa Oraji) |
| 16:00 | 16:30 | [**Review of MPI Continuations and Their Integration into PMPI Tools.**][optenhoefel] (Alexander Optenhöfel) |
| 16:30 | 17:00 | [**Extending the SPMD IR for RMA Models and Static Data Race Detection.**][burak] (Semih Burak) |

## Oct 2 - Day 2

| Start | End   | Session |
|-------|-------|---------|
| 8:30  | 9:00  | Registration & Coffee |
| **9:00**  | **10:00**  | **Joint Keynote II - Bob Lucas (Ansys)** |
| 10:00 | 10:30 | Coffee Break |
| **10:30** | **11:30** | **Session II: Language Support (C++)** |
| 10:30 | 11:00 | **Layout-Agnostic MPI Abstraction for Distributed Computing in Modern C++.** (Jiří Klepl) |
| 11:00 | 11:30 | **Concepts for designing modern C++ interfaces for MPI** (C. Nicole Avans) |
| **11:30** | **12:00** | [**Lessons from MPICH**][gropp] (Bill Gropp, Invited Talk) |
| 12:00 | 13:30 | **Lunch Break with Poster Session** |
| **13:30** | **15:00** | **Session III: Performance** |
| 13:30 | 14:00 | [**On the Potential of Compression Hiding in MPI Applications**][li] (Yicheng Li) |
| 14:00 | 14:30 | **Implementing True MPI Sessions and Evaluating MPI Initialization Scalability** (Hui Zhou) |
| 14:30 | 15:00 | **Performance analysis of OpenMPI on AMR applications over Slingshot-11** (Maxim Moraru) |
| 15:00 | 16:00 | Break |
| 16:00 |       | Bus pickup (location TBA) |
| 16:30 |       | **Social Event: [NASCAR museum](https://www.nascarhall.com/)** |

## Oct 3 - Day 3

| Start | End   | EuroMPI / IWOMP |
|-------|-------|-----------------|
| 8:30  | 9:00  | Registration & Coffee |
| **9:00**  | **10:00**  | **Joint Keynote III: TBD** |
| 10:00 | 10:30 | Coffee Break |
| **10:30** | **11:30** | **Session IV: Multi-Threading** |
| 10:30 | 11:00 | **Examine MPI and its Extensions for Asynchronous Multithreaded Communication** (Jiakun Yan) |
| 11:00 | 11:30 | **MPI Finally Needs to Deal with Threads** (Joseph Schuchart) |
| **11:30** | **12:00** | **Panel: TBD** |
| 12:00 | 13:30 | Lunch Break |
| **13:30** | **14:30** | **Open Discussions** |
| 14:30 | 15:45 | Closing Remarks and Goodbye |
