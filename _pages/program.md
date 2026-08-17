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
    <td>Session I</td>
    <td>Session I</td>
  </tr>

  <tr class="program-break">
    <td>12:00–13:30</td>
    <td colspan="2">Lunch</td>
  </tr>

  <tr>
    <td>13:30–15:00</td>
    <td>Session II</td>
    <td>Session II</td>
  </tr>

  <tr>
    <td>15:00–15:15</td>
    <td>Poster Short Presentations</td>
    <td class="program-break">Coffee Break</td>
  </tr>

  <tr class="program-break">
    <td>15:15–15:30</td>
    <td colspan="2">Euro MPI Posters &amp; Coffee Break</td>
  </tr>

  <tr>
    <td>15:30–17:00</td>
    <td>Posters</td>
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
      <p>High performance computing (HPC) has long driven breakthroughs in physics, chemistry, and engineering. Today, the emergence of digital twins in healthcare introduces a new frontier: personalized, physics-informed simulations of the human vascular system. These models demand solving fluid dynamics over complex 3D anatomies across millions of heartbeats, while integrating continuous data from wearable sensors. The result is petabyte-scale datasets and real-time simulation needs that stretch the limits of algorithms, data handling, and scalability. This keynote will highlight how vascular digital twins expose new challenges and opportunities for HPC—reducing communication overhead in parallel time integration, compressing multimodal data streams without losing fidelity, and enabling adaptive, continuous simulation at exascale. Meeting these challenges requires leadership-scale systems co-designed with novel algorithms and workflows. Beyond medicine, these lessons illustrate how HPC can evolve to support time-critical, data-rich applications across domains, underscoring the need for sustained investment and long-term vision in high performance computing.</p>

      <p><strong>Florina M. Ciorba</strong>: Florina M. Ciorba is Professor of High Performance Computing and head of the HPC Lab at the University of Basel, Switzerland, which she founded in 2015. She earned her Ph.D. from the National Technical University of Athens, Greece in 2008, followed by postdoctoral positions at Mississippi State University, USA, and Dresden University of Technology, Germany. Her research focuses on scheduling and resource management, and on enhancing performance, resilience, portability, reproducibility, and autonomy in HPC and AI/ML systems. Recent work includes autotuning, energy-efficient cosmological simulations, and autonomy loops for system performance. Her group developed LB4OMP and Auto4OMP, open-source extensions of the LLVM OpenMP runtime for dynamic loop scheduling and automated scheduling algorithm selection. She has published nearly 100 peer-reviewed papers and received several best paper awards. She is a founding board member and PI of the Basel node in the SKACH project (Swiss SKAO Consortium) and co-founded IDEAS4HPC, the Swiss chapter of Women in HPC. She also serves on other various boards and committees related to HPC and energy efficiency. She is a senior & life member of ACM and active in IEEE, HiPEAC, and DISCOVER-US.  More at <a href="http://hpc.dmi.unibas.ch/">http://hpc.dmi.unibas.ch</a>.</p>
      </details>
    </td>
  </tr>

  <tr class="program-break">
    <td>10:00–10:30</td>
    <td colspan="2">Coffee Break</td>
  </tr>

  <tr>
    <td>10:30–12:00</td>
    <td>Session III</td>
    <td>Session IV</td>
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
    <td>Session IV</td>
    <td>Session VI</td>
  </tr>
</tbody>

</table> </div>

<h2>Friday, 9 October 2026</h2>

<div class="program-day"> <table class="program-table"> <thead> <tr> <th class="program-time">Time</th> <th>EuroMPI</th> <th>IWOMP</th> </tr> </thead> <tbody> <tr class="program-registration"> <td>08:30–09:00</td> <td colspan="2">Registration &amp; Coffee</td> </tr>

  <tr class="program-keynote">
    <td>09:00–10:00</td>
    <td colspan="2"><strong>Joint Keynote 3:</strong> TBA</td>
  </tr>

  <tr>
    <td>10:00–11:00</td>
    <td>Session V</td>
    <td>Session VII</td>
  </tr>

  <tr class="program-break">
    <td>11:00–11:30</td>
    <td colspan="2">Coffee Break</td>
  </tr>

  <tr class="program-panel">
    <td>11:30–12:30</td>
    <td colspan="2"><strong>Joint Panel:</strong> TBA</td>
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

