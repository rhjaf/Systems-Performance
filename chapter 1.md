Definitions of Performance:
- Performance concerns about $Observability$ and $Performance Tools$
- Systems Performance means (hw+sw=full-stack) or entire $datapath$. Its goal is to improve user expericnce by reducing latency and costs
- Software Development Cycle - from concept to deply: In this book we cover $metholodies$ and $tools$ for these steps.
  1. set performance objective/mode
  2. performance characterization of prototype
  3. performance analysis of in-development product in test environment
  4. non regression test for new versions
  5. benchmark analysis
  6. test in production environment
  7. performance tunning
  8. monitoring
  9. performance analysis of production issues
  10. incident review of production issues
  11. use or develop performance tools to enhance production
  Stpes 1-5 are always executed. But by arising cloud platforms, It is not needed to do these steps and jump forward to step 6
  - canary testing: one component test
  - blue-green test: bring up a copy version to perform develop on it while the current stable product works
  - steps 9 and 10 are like developer's retrospective mettings.
- Another performance categories:
    - workload: developers
    - resources: system administrators
- Performance challenges:
    - $subjective$: againts $objectivity$ (black-white things) of software troubleshooting. solutions: define goals to convert to objectivitiy. ex: avg disk IO response time is 1m ==> less than 2m is required
    - comples: no start point for systems. solution: use methodologies
    - no single root issue: which issue matters most
Observibility:
- counters: usually hardcoded in software or kernel's code for storing current state. eg: `vmstat`
- profiling(statistics,metrics) : drawing graphs from target 
- tracing: event-base. eg: `tcpdump`, `strace`, `bpftrace`, `BCC`,
    - BPF is programmable
    - static/dynamic instrumentation
