---
permalink: program
---

<script type="text/javascript" src="/assets/js/timeconvert.js"></script>

![Banner](/assets/Vienna.png){:height="auto" width="100%"}

<style>
  .program-intro {
    margin-bottom: 2em;
    padding: 1em 1.25em;
    border-left: 4px solid #999;
    background: #f7f7f7;
  }

  .program-day {
    margin-bottom: 3em;
    overflow-x: auto;
  }

  .program-table {
    width: 100%;
    border-collapse: collapse;
    margin-bottom: 1em;
    font-size: 0.95em;
  }

  .program-table th,
  .program-table td {
    padding: 0.75em 0.8em;
    border-bottom: 1px solid #ddd;
    vertical-align: middle;
  }

  .program-table thead th {
    font-weight: 700;
    text-align: left;
    border-bottom: 2px solid #999;
  }

  .program-table .program-time {
    width: 12%;
    white-space: nowrap;
  }

  .program-table tbody td:first-child {
    white-space: nowrap;
    font-weight: 600;
  }

  .program-break td {
    background: #f7f7f7;
    font-style: italic;
    text-align: center;
  }

  .program-registration td {
    background: #f7f7f7;
  }

  .program-keynote td,
  .program-panel td {
    font-weight: 600;
  }

  .program-social td {
    padding-top: 1em;
    padding-bottom: 1em;
    font-weight: 600;
  }

  .program-welcome .program-end td {
    font-weight: 700;
  }

  @media screen and (max-width: 600px) {
    .program-table {
      font-size: 0.9em;
    }

    .program-table th,
    .program-table td {
      padding: 0.6em;
    }

    .program-table .program-time {
      width: 15%;
    }
  }

  .program-table th:nth-child(2),
  .program-table td:nth-child(2) {
    border-left: 1px solid #ddd;
    padding-left: 1.5em;
  }

  .program-table th:nth-child(3),
  .program-table td:nth-child(3) {
    border-left: 1px solid #ddd;
    padding-left: 1.5em;
  }

  .program-table {
  width: 100%;
  table-layout: fixed;
  border-collapse: collapse;
  }

  .program-table th:nth-child(2),
  .program-table td:nth-child(2),
  .program-table th:nth-child(3),
  .program-table td:nth-child(3) {
    width: 42.5%;
  }
  .talk {
    margin-bottom: 1em;
    padding-bottom: 1em;
    border-bottom: 1px solid #ddd;
  }

  .talk:last-child {
    border-bottom: none;
    margin-bottom: 0;
  }

  .talk-presenter {
    font-style: italic;
  }
</style>



<div class="program-intro"> <p> The <strong>EuroMPI &amp; IWOMP 2026</strong> preliminary program is available below. </p>

<p> The program is <strong>preliminary and subject to change</strong>. Detailed session information, including individual talks and speakers, will be added as the program is finalized. </p> </div>

<h2>Wednesday, 7 October 2026</h2>

<div class="program-day"> <table class="program-table">
<thead>
  <tr>
    <th class="program-time">Time</th>
    <th>EuroMPI</th>
    <th>IWOMP</th>
  </tr>
</thead>

<tbody>
  <tr class="program-registration">
    <td>08:30–08:55</td>
    <td colspan="2">Registration &amp; Coffee</td>
  </tr>

  <tr class="program-welcome">
    <td>08:55–09:00</td>
    <td colspan="2">Welcome</td>
  </tr>

  <tr class="program-keynote">
    <td>09:00–10:00</td>
    <td colspan="2"><strong>Joint Keynote 1:</strong> TBA</td>
  </tr>

  <tr class="program-break">
    <td>10:00–10:30</td>
    <td colspan="2">Coffee Break</td>
  </tr>

  <tr>
    <td>10:30–12:00</td>
    <td class="session-title">Session I: Language Interfaces</td>
    <td>Session I</td>
  </tr>

  <tr>
    <td></td>
    <td>
      <div class="talk">
        <span class="talk-title">Core MPI</span><br>
        <span class="talk-presenter">Hui Zhou</span>
        <details>
        <summary>Abstract</summary>
        <p class="talk-abstract">
        </p>The latest MPI standard defines 677 functions, most of which see limited adoption, while long-recognized capabilities such as fault tolerance and stream-triggered communication remain absent. At the same time, implementations struggle to sustain an ever-expanding specification. We argue that these issues share a common cause: MPI’s specification is broad but conceptually flat. We propose Core MPI, a constructive reformulation based on three principles: assumed collective agreement by program construction, progressive exposure of operation internals, and runtime foundation through interface exposure. Together, these principles define a minimal core API while positioning MPI to support runtimes built on top of it rather than absorbing them within MPI. Guided by this framework, we show how long-pending proposals such as ULFM and stream-triggered communication can be positioned and thereby have clearer paths toward adoption. The goal is not to reduce MPI, but to provide a framework for evaluating new extensions, organizing implementations around a stable core with independent higher-level layers, and supporting MPI’s continued evolution to meet
        </details>
      </div>

      <div class="talk">
        <span class="talk-title">Concepts in Practice: C++ MPI Bindings for the HPC Ecosystem. From a Standardizable Core to a Composable Interface</span><br>
        <span class="talk-presenter">Tim Niklas Uhl</span>
        <details>
        <summary>Abstract</summary>
        <p class="talk-abstract">The official C++ MPI bindings were removed from the standard in 2008, leaving a gap that numerous third-party libraries have attempted to fill. However, existing wrappers typically cover only a limited subset of MPI or target specific use cases, falling short of a general-purpose solution. A recent conceptual paper proposed general design principles for modern C++ bindings based on C++20 concepts, without committing to a concrete interface. We present the first concrete realization of these principles in a layered architecture. At the foundation, we define a core layer: refined C++20 concepts formalizing the MPI standard's notion of data buffers, automatic mapping of standard C++ constructs, non-intrusive customization points for third-party types, and concept-based wrappers for MPI procedures. The result is a low-level native C++ MPI interface that works directly with STL containers, is highly extensible, and lends itself to standardization. Built on this core, we present KamPing v2 - a C++ MPI library offering the convenience and memory-safety of KaMPIng with composable, pipe-based syntax inspired by C++ ranges for efficient, boilerplate-free MPI programming. Finally, we demonstrate the core layer's broad applicability by designing lightweight adapters for GPU and performance-portability libraries, making the HPC ecosystem a first-class citizen in MPI. Kokkos views, Thrust device vectors, and SYCL buffers can be passed directly to MPI procedures, with adapter logic remaining self-contained. All contributions are backed by a fully functional open-source reference implementation, demonstrating the practical viability of the proposed design.
        </p>
        </details>
      </div>

      <div class="talk">
        <span class="talk-title">Write Once, Communicate Anywhere: API Design for Performance-Portable Communication</span><br>
        <span class="talk-presenter">Gabriel Dos Santos</span>
        <details>
        <summary>Abstract</summary>
        <p class="talk-abstract">The High Performance Computing communication landscape is fragmented: MPI dominates network-level communication while device-native collective libraries (NCCL and RCCL) are purpose-built for GPU-to-GPU operations. Existing interfaces do not provide this combination of single-source backend portability, modern C++ data abstractions, and unified execution semantics, leaving users to bridge distinct data and execution models manually. This paper presents a unified API design that bridges this gap, enabling portable communication between MPI and NCCL/RCCL from a single source codebase. The interface consists of a compact subset of MPI operations, closely matching what NCCL/RCCL supports, as a deliberate design choice to ensure semantic consistency across backends. We leverage C++20 compile-time facilities to achieve zero overhead abstraction relative to a library-specific, hand-written solution. Integrated with the Kokkos programming model, we provide View-aware communication primitives that avoid manual object decomposition, and a unified completion model that resolves execution model discontinuities. We demonstrate the concrete realization of this design with the Kokkos Comm library. To our knowledge, Kokkos Comm is the first C++ API design to combine single-source portability across MPI and NCCL/RCCL with View-aware communication and deep integration into a performance-portable execution framework.
        </p>
        </details>
      </div>
    </td>
    <td>
    </td>
  </tr>

  <tr class="program-break">
    <td>12:00–13:30</td>
    <td colspan="2">Lunch</td>
  </tr>

  <tr>
    <td>13:30–15:00</td>
    <td class="session-title">Session II: Correctness and Performance Profiling</td>
    <td>Session II</td>
  </tr>

  <tr>
    <td></td>
    <td>
      <div class="talk">
        <span class="talk-title">Allocation Tracking and Parameter Checking for Parallel Programming Models using Contracts</span><br>
        <span class="talk-presenter">Yussur Mustafa Oraji</span>
        <details>
        <summary>Abstract</summary>
        <p class="talk-abstract">Correctness checking tools for High-Performance Computing programs are typically limited to specific parallel programming models such as MPI or OpenSHMEM. The CoVer framework previously addressed this by introducing a generic, contract-based approach that decoupled API requirements from the core tool. However, CoVer's effectiveness remains bounded by the expressiveness of its underlying contract language, restricting the types of errors it can verify. This paper presents an extension to the CoVer contract language designed to capture and check a broader range of error classes. Our extensions introduce generic parameter checking and allocation tracking, while keeping generality across both programming model and language. We evaluate these extensions and demonstrate that analysis accuracy remains consistent across multiple languages, reinforcing the framework's general applicability. While the additional runtime analyses naturally incur a performance overhead, these improvements greatly enhance CoVer's utility with a significant accuracy improvement.
        </p>
        </details>
      </div>

      <div class="talk">
        <span class="talk-title">How Caching Distorts MPI Point-to-Point Performance</span><br>
        <span class="talk-presenter">Niklas Bartelheimer</span>
        <details>
        <summary>Abstract</summary>
        <p class="talk-abstract">Applications on modern high-performance computing (HPC) systems rely heavily on the Message Passing Interface (MPI) for inter-process communication. In this work, we demonstrate that CPU cache hierarchies can introduce a substantial and previously overlooked influence on the execution time of MPI point-to-point communication routines and thus their performance. To investigate these effect, we introduce Cold Cache MPI (ccMPI), a custom microbenchmark suite designed to isolate cache-related influences. We evaluate send and receive operations under varying cache states across three different HPC network technologies: TofuD, Omni-Path, and InfiniBand. Our results show that performance degradation is driven primarily by cold last-level cache conditions, where misses result in expensive main-memory accesses. In contrast, the cache locality of the user message buffer often has limited impact, while keeping MPI-internal data structures resident in cache can significantly reduce latency for large messages. We further observe that transport protocol design choices, especially the bounce-buffer usage in eager protocols and host-driven transfer mechanisms (onloading model used by Omni-Path), introduce additional cache sensitivities. These findings underline the importance of considering processor microarchitectural behavior when evaluating and optimizing MPI communication performance.
        </p>
        </details>
      </div>
    </td>
    <td></td>
  </tr>

  <tr class="program-break">
    <td>15:00–15:30</td>
    <td colspan="2">Coffee Break</td>
  </tr>

  <tr>
    <td>15:30–17:00</td>
    <td>Poster Short Presentations &amp; Posters</td>
    <td>Session III</td>
  </tr>

  <tr class="program-social">
    <td>19:00</td>
    <td colspan="2">
      <strong>Social Event</strong><br>
      EuroMPI &amp; IWOMP Joint Dinner
    </td>
  </tr>
</tbody>

</table> </div>

<h2>Thursday, 8 October 2026</h2>

<div class="program-day"> <table class="program-table"> <thead> <tr> <th class="program-time">Time</th> <th>EuroMPI</th> <th>IWOMP</th> </tr> </thead> <tbody> <tr class="program-registration"> <td>08:30–09:00</td> <td colspan="2">Registration &amp; Coffee</td> </tr>

  <tr class="program-keynote">
    <td>09:00–10:00</td>
    <td colspan="2"><strong>Joint Keynote 2:</strong> Who Decides? Beyond Runtime Defaults, Toward Adaptive Multi-Device OpenMP<br>
      <i>Florina M. Ciorba, University of Basel</i>
      <details>
      <summary>Abstract</summary>
      <p>OpenMP has spent two decades making parallelism expressible. The harder question now is who decides how that parallelism is exploited. Every OpenMP program already delegates its most important choices (which schedule and chunk size, which task runs next, which device, how many teams) to a compiler, a runtime, an operating system, and a batch scheduler, and these rarely talk to one another. On heterogeneous multi-device systems, and with irregular, AI-augmented workloads, those choices can no longer be made once, statically, by whoever wrote or implemented the directive.<br>

      In our group we took the auto schedule kind (OpenMP's solution to scheduling choices it cannot know in advance) and asked what it would take to make it mean something.  Our LB4OMP library brought a portfolio of dynamic and adaptive self-scheduling algorithms into the LLVM OpenMP runtime; its extension, Auto4OMP, added expert-based and reinforcement-learning selection of both algorithm and chunk parameter, per loop, per time step, per platform. 
      The loop is where the problem is easiest to measure; tasking and device offloading raise the same question, and neither has answered it. I will show what we learned from applying this work to real scientific simulations, and from measuring how application and operating-system schedulers interfere with one another.<br>

      I will argue that adaptivity in OpenMP must become first-class, observable, and cross-layer. A wrong default is not only slow: it strands portable code on the next device, pushes performance tuning back to the scientist, and burns energy at every time step. Performance, portability, productivity, and sustainability are not four separate concerns but are decided together, each time work meets a device.</p>

      <p><strong>Florina M. Ciorba</strong>: Florina M. Ciorba is Professor of High Performance Computing and head of the HPC Lab at the University of Basel, Switzerland, which she founded in 2015. She earned her Ph.D. from the National Technical University of Athens, Greece in 2008, followed by postdoctoral positions at Mississippi State University, USA, and Dresden University of Technology, Germany.<br>
      Her research focuses on scheduling and resource management, and on enhancing performance, resilience, portability, reproducibility, and autonomy in HPC and AI/ML systems. Recent work includes autotuning, energy-efficient cosmological simulations, and autonomy loops for system performance. Her group developed LB4OMP and Auto4OMP, open-source extensions of the LLVM OpenMP runtime for dynamic loop scheduling and automated scheduling algorithm selection. She has published nearly 100 peer-reviewed papers and received several best paper awards.<br>
      She is a founding board member and PI of the Basel node in the SKACH project (Swiss SKAO Consortium) and co-founded IDEAS4HPC, the Swiss chapter of Women in HPC. She also serves on other various boards and committees related to HPC and energy efficiency. She is a senior & life member of ACM and active in IEEE, HiPEAC, and DISCOVER-US.  More at <a href="http://hpc.dmi.unibas.ch/">http://hpc.dmi.unibas.ch</a>.</p>
      </details>
    </td>
  </tr>

  <tr class="program-break">
    <td>10:00–10:30</td>
    <td colspan="2">Coffee Break</td>
  </tr>

  <tr>
    <td>10:30–12:00</td>
    <td class="session-title">Session III: Collective Operations and Algorithms</td>
    <td>Session IV</td>
  </tr>
  
  <tr>
    <td></td>
    <td>
      <div class="talk">
        <span class="talk-title">Effective MPI: User-defined Datatypes and Cartesian Communicators for Zero-copy All-to-all Communication in Multidimensional Tori</span><br>
        <span class="talk-presenter">Jesper Larsson Träff</span>
        <details>
        <summary>Abstract</summary>
        <p class="talk-abstract">We present and show how to implement a non-trivial all-to-all communication algorithm for arbitrary d-dimensional tori effectively in MPI. Given a factorization of the number of processes p into d factors that can be mapped onto a d-dimensional torus, we first utilize a Cartesian communicator to split a given p-process MPI communicator into, for each MPI process, d smaller communicators spanning each of the dimensions of the torus to which the process belongs, and cache these communicators in order to avoid expensive splitting at each all-to-all operation. The all-to-all operation itself is decomposed into a sequence of d MPI alltoall operations on the dimension-wise communicators. The non-trivial data rearrangement before and after each MPI alltoall call is implicit only and effected by MPI derived datatypes. This makes the implementation of the algorithm formally zero-copy, meaning that no explicit process-local reordering of data blocks ever has to be performed. In order to achieve this, the algorithm employs a double-buffering scheme with modest temporary buffer requirements. By choosing the factorization of p and selecting appropriate implementations for the component MPI alltoall operations, the presented implementation gives ample opportunities for algorithm tuning and adaptation to the particular high-performance system. A few, select experimental results show competitive performance with native MPI alltoall implementations and illustrate problems that common MPI alltoall implementations may have.
        </p>
        </details>
      </div>

      <div class="talk">
        <span class="talk-title">A Unified Two-Dimensional Design Space for the MPI All-to-All Collective</span><br>
        <span class="talk-presenter">Ke Fan</span>
        <details>
        <summary>Abstract</summary>
        <p class="talk-abstract">The all-to-all collective sits on the critical path of many HPC and ML workloads, and its performance is highly sensitive to the process count P and the message size N. Prior work has made two parameters tunable, but never both in the same algorithm. The radix r is tuned in blocking round-by-round schedules, trading the number of rounds against the exchanged volume. The batch-size b, in contrast, is tuned in non-blocking batched schedules, trading network contention against concurrency. We find that the two can coexist in a single schedule, once these structurally divergent paradigms are reconciled. We do so by observing that the true dependency holds only across phases, leaving same-phase steps free to batch. On this basis we present GATA (Generalized All-To-All), a uniform all-to-all algorithm that tunes r and b jointly over a dense two-dimensional design space. Widely-deployed algorithms occupy only the boundary of this space, while its interior exposes configurations none of them can express. Selecting an all-to-all algorithm therefore becomes a matter of tuning two parameters within a single implementation. On Polaris at up to 8192 processes, the slowest and fastest (r, b) configurations at a fixed (P, N) differ by as much as 683 times. Once tuned, GATA outperforms the strongest baseline by up to 3.4 times and the vendor-optimized MPI alltoall by up to 10.6 times.
        </p>
        </details>
      </div>

      <div class="talk">
        <span class="talk-title">The Allgather-merge Collective Operation: Algorithms, Implementation, Performance</span><br>
        <span class="talk-presenter">Leonhard Ender</span>
        <details>
        <summary>Abstract</summary>
        <p class="talk-abstract">In the collective allgather-merge operation, which has been used as a building block for efficient sorting algorithms, each process in a collection of processes contributes a sorted input array; the contributions are merged together and each process is returned the full, sorted array (with or without removal of duplicates). We present the allgather-merge operation as an MPI-like collective operation, and give a stepwise development of an efficient algorithm. In the regular version of the operation, where each of the p processes contributes approximately m/p elements, the final algorithm takes time O(m+log(p)), in contrast to the O(m log(p)) time taken by the baseline algorithm, and works uniformly for any number of MPI processes. The stepwise improvement over the baseline algorithm implemented in terms of MPI allgather and p-way process-local merge leads to improvements in completion time of 50% in benchmarks on a small 36x32 core cluster.
        </p>
        </details>
      </div>
    </td>
    <td></td>
  </tr>

  <tr class="program-break">
    <td>12:00–13:30</td>
    <td colspan="2">Lunch</td>
  </tr>

  <tr>
    <td>13:30–14:30</td>
    <td>Invited Talk</td>
    <td rowspan="2">Session V</td>
  </tr>

  <tr>
    <td>14:30–15:00</td>
    <td>---</td>
  </tr>

  <tr class="program-break">
    <td>15:00–15:30</td>
    <td colspan="2">Coffee Break</td>
  </tr>

  <tr>
    <td>15:30–17:00</td>
    <td class="session-title">Session IV: MPI Extensions and Data Compression</td>
    <td>Session VI</td>
  </tr>
  
  <tr>
    <td></td>
    <td>
      <div class="talk">
        <span class="talk-title">Making MPI Collectives Pluggable</span><br>
        <span class="talk-presenter">Carsten Clauss</span>
        <details>
        <summary>Abstract</summary>
        <p class="talk-abstract">Modern HPC and machine-learning workloads increasingly rely on specialized collective communication libraries such as UCC, Gloo, and/or accelerator backends like NCCL, RCCL, oneCCL. However, current MPI implementations expose no public mechanism for integrating external collective algorithms, limiting interoperability and preventing applications from exploiting domain-specific optimizations. This paper presents a new registration-based approach that opens the collective layer of ParaStation~MPI to user-defined algorithms in a pluggable manner, where the registered algorithms can be used just like regular collectives, but also internally by the MPI library itself, for example, for mapping one collective to the pattern of another. The proposed design is a generic MPI extension for registering, selecting, and executing external collective algorithms while preserving full MPI semantics. To demonstrate the generality of this approach, we have implemented three independent plugins that leverage this interface extension: (1) a high-accuracy MPI reduction algorithm based on binned summation, (2) a UCC backend based on the existing UCC integration in MPICH, and (3) a prototype backend for the PyTorch-related Gloo collective communications library. While the first example demonstrates that the proposed interface can be useful for MPI applications that implement their own collective operations, the second example illustrates that also third-party backends can be integrated effectively and portably via the same interface; and the latter also applies to the third backend, which represents, to the best of our knowledge, the first inclusion of Gloo by an MPI library.
        </p>
        </details>
      </div>

      <div class="talk">
        <span class="talk-title">Extending MPI for Portable Payload Compression</span><br>
        <span class="talk-presenter">Carsten Clauss</span>
        <details>
        <summary>Abstract</summary>
        <p class="talk-abstract">The emergence of heterogeneous and modular Exascale systems is fundamentally changing the performance characteristics of large-scale scientific applications. While computational throughput continues to increase through massive parallelism and the integration of accelerators, data movement and communication are increasingly dominating overall runtime and energy consumption. This imbalance is particularly noticeable in data-intensive simulation codes, where large multidimensional fields must be exchanged frequently between distributed processes. Data reduction through compression is one possible measure to counteract this imbalance. The Message-Passing Interface (MPI) standard has been the predominant programming model for high-performance computing architectures with distributed memory for many years now, thanks to its scalability and performance, but especially due to its portability and hardware-independent design principles. However, these same principles pose a challenge when integrating data reduction techniques directly into MPI in a platform-independent and portable way, while allowing for application-specific choices of compression algorithms and parameters at the same time. This is especially true when it comes to lossy compression, where acceptable error and performance trade-offs require close coordination between the application, the compressor, and the MPI library. In this paper, we present a proposal for MPI extensions that enable such a tight but generic and standard-oriented integration of algorithms for MPI payload compression via the registration of callback functions and their control via MPI info hints. To this end, we present a prototype implementation of these extensions in ParaStation~MPI, a high-performance MPICH derivative, and discuss and demonstrate their usability and generality with two different compressor implementations.
        </p>
        </details>
      </div>

      <div class="talk">
        <span class="talk-title">Adaptive compression techniques for ad-hoc parallel file systems based on MPI</span><br>
        <span class="talk-presenter">Dario Muñoz-Muñoz</span>
        <details>
        <summary>Abstract</summary>
        <p class="talk-abstract">The exponential growth of data-intensive workloads in high-performance computing has led to severe bottlenecks in traditional shared parallel file systems. As a high-performance alternative, ad-hoc parallel file systems leverage local node resources to provide ephemeral, low-latency storage. To achieve maximum portability and peak performance, some ad-hoc solutions rely on MPI as their underlying communication engine. However, because these ad-hoc file systems are located on the same compute nodes as the applications, they introduce critical resource contention. Both layers (application and ad-hoc file system) simultaneously compete for the same local storage, CPU, and MPI network infrastructure, which can degrade overall application throughput. This work addresses these limitations by introducing an adaptive compression technique explicitly designed to mitigate co-location contention in MPI-based ad-hoc storage. The core of this approach is an intelligent mechanism that dynamically decides when to compress data before transmission and stores it in a compressed format on the target server. Thereby reducing the data volume traversing the network and optimizing the limited local storage resources, minimizing the interference caused by the ad-hoc file system during application execution. To validate this approach, the proposed solution was integrated into Expand Ad-Hoc, an ad-hoc parallel file system that relies on an MPI client-server architecture and standard MPI. Evaluated on the C3 supercomputer using the IOR benchmark and the Nek5000 computational fluid dynamics application, our results demonstrate that adaptive compression significantly reduces network and disk contention. When data is compressed by half, write performance improves by 148% and read performance by 29%, highlighting the critical role of data reduction strategies in optimizing MPI-communicating storage software.
        </p>
        </details>
      </div>
    </td>
    <td></td>
  </tr>

</tbody>

</table> </div>

<h2>Friday, 9 October 2026</h2>

<div class="program-day"> <table class="program-table"> <thead> <tr> <th class="program-time">Time</th> <th>EuroMPI</th> <th>IWOMP</th> </tr> </thead> <tbody> <tr class="program-registration"> <td>08:30–09:00</td> <td colspan="2">Registration &amp; Coffee</td> </tr>

  <tr class="program-keynote">
    <td>09:00–10:00</td>
    <td colspan="2"><strong>Joint Keynote 3:</strong> Experiences with AI-Driven Development in HPC Software<br>
      <i>Jeff Hammond, NVIDIA</i>

      <details><summary>Abstract</summary>
      <p>Agentic development has progressed rapidly over the past two years, to the point where it makes sense to ask whether AI can write complex communication software by itself. In this talk, I will describe my experience building an MPI library from scratch using AI. With expert guidance on design and testing, AI was able to implement all of MPI-5 from scratch in less than a month, with support for shared-memory, sockets, OFI/libfabric and UCX, with optimized algorithms for message matching, collectives, etc. I will also talk about agentic development of GPU communication software based on NCCL and NVSHMEM, demonstrating that AI is not limited to CPU environments.</p>

      <p><strong>Jeff Hammond</strong> is a Distinguished Engineer at NVIDIA in the data center software organization, focused on GPU communications (NCCL and NVSHMEM). He has extensive experience with the design and use of parallel programming models and scientific applications. Jeff’s most notable achievements include the MPI-5 Application Binary Interface standard, development of the MPI-3 one-sided communication software ecosystem, and contributions to the NWChem quantum chemistry project. He received a PhD in Chemistry from the University of Chicago in 2009.</p>
      </details>
    </td>
  </tr>

  <tr>
    <td>10:00–11:00</td>
    <td colspan="2">
      <div class="session-title">Joint EuroMPI &amp; IWOMP session</div>
    </td>
  </tr>
  <tr>
    <td></td>
    <td>
      <div class="talk">
        <span class="talk-title">Leveraging the MPI ABI for Binary-Level Detection of MPI Traits</span> (EuroMPI 2026 best paper)<br>
        <span class="talk-presenter">Tim Jammer</span>
        <details>
        <summary>Abstract</summary>
        <p class="talk-abstract">Many runtime optimizations and correctness guarantees rely on global program properties that must hold across an application and all dynamically linked components. In compositional software systems, where binaries are assembled at load time from independently built libraries, such properties are difficult to verify, often forcing conservative assumptions. For MPI, this becomes relevant for the usage of matching wildcards, for example. More optimized message matching may be possible, if no wildcards are used. Traditionally, establishing such properties across all components requires source code access or whole-program analysis. With the introduction of a stable MPI application binary interface (ABI), we argue that this reasoning can be shifted to the binary level. In this work, we present two complementary approaches to detect the absence of wildcard usage in dynamically linked MPI applications: an explicit approach based on lightweight binary markers and an implicit approach based on static disassembly analysis. We evaluate both methods on real-world MPI applications. Our results show that binary-level detection at MPI startup incurs only limited overhead, ranging from 0.2% to 8% of MPI initialization time, depending on the approach. We further discuss trade-offs in terms of reliability, portability, and extensibility. Overall, our work demonstrates that binary-level trait detection is a practical mechanism for enabling cross-component reasoning in modern MPI applications.
        </p>
        </details>
      </div>
    </td>
    <td>TBA
    </td>
  </tr>


  <tr class="program-break">
    <td>11:00–11:30</td>
    <td colspan="2">Coffee Break</td>
  </tr>

  <tr class="program-panel">
    <td>11:30–12:30</td>
    <td colspan="2"><strong>Joint Panel:</strong> What does AI with and can it provide for standards?</td>
  </tr>

  <tr>
    <td>12:30–12:45</td>
    <td>Closing Remarks</td>
    <td></td>
  </tr>

  <tr class="program-break">
    <td>12:45–14:00</td>
    <td colspan="2">Lunch</td>
  </tr>

  <tr class="program-end">
    <td>14:00</td>
    <td colspan="2"><strong>End of Conference</strong></td>
  </tr>
</tbody>

</table> </div>

<p class="info-box"> <strong>Note:</strong> This is a preliminary program. Session titles, speakers, timings and room assignments may change. The final program will be published closer to the conference. </p>

