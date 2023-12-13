---
layout: cv
title: Adam Mozes's CV
---
# Adam Mozes
Senior Rust Engineer, Arbitrage finder, Amateur powerlifter / weightlifter, Jack of all trades

<div id="webaddress">
<a href="mailto:mozes.adam.istvan@proton.me">E-mail</a>
| <a href="https://nvxxu2i.github.io/markdown-cv">CV (web)</a>
| <a href="javascript:window.print()">CV (printed)</a>
| <a href="https://linkedin.com/in/mozesadamistvan">LinkedIn</a>
</div>

## Who am I?
I am Adam, a seasoned senior software engineer, with experiences from various
fields, which can make me a great generalist.
I usually thrive in high-impact roles, especially in the strategic ones, when
different viewpoints have to be integrated in a single decision, and the
mastery of trade-offs are required.

My current interest and hobby is writing low-latency Rust code in the trading
space, which combines software development, operations, and investments in a
single hobby.

## Highlighted experiences
### Stealth-stage trading desk
`March 2023 - present`
__Founder__, London, United Kingdom

- Back in 2018, Rust-related jobs were virtually non-existent, and I wanted to
  learn the language in a more practical project, and had some ideas of
  technical analysis, so a cryptocurrency market predictor was born.
- After several rewrites and its failed predictions, this project was reborn as
  a simple arbitrage finder between certain exchanges, harvesting those tiny,
  short-lived mispricings, without introducing significant risks caused by the
  market movements.
- From a business perspective: The average monthly trading volume is between
  \$600,000 and \$1,000,000, while the operating costs are less than \$200. On
  a good week, the daily returns are around 0.5%.
- As of this moment, this project is still in its infancy in terms of
  profitability, but at least it exposed me to various interesting technical
  challenges, and where I must carefully choose my moves as I have skin in the
  game.
- _Keywords_: Rust, Arch Linux, systemd, REST, FIX, systemd, AWS, arbitrage,
  delta-neutral

### Commsignia
`August 2020 - April 2021`
__Software Architect__, Budapest, Hungary

- Mission: Commsignia launched a new remote command-and-control product for the
  deployed Road Side Units. This had to be delivered within six months as it
  has been sold to Hungarian Public Roads Ltd. The team was non-existent at
  this point, and careful planning and execution were paramount.
- I had no structured knowledge of how to design maintainable architecture, so
  the first thing I did was to read through Robert C. Martin's: Clean
  Architecture, and as suggested, I wanted to defer decisions as late as
  possible to avoid painting ourselves into a corner.
- Due to some external forces, we had to write the majority of the code in Java
  (and I still have little hands-on experience in Java), so a Lead Developer
  had to be recruited as my peer, who can execute and decide on the
  implementation details.
- I have created a control and a command plane and defined tens of modules with
  their clear concerns and the expected interface between them as fast as
  possible so that development can be started with some selected modules.
- Due to the sensitive nature of this project, I had to integrate this product
  into the _Hungarian Public Roads_ network, which included late-stage
  debugging, as it even required being on-call.
- Conclusion: This project was a success and brought significant revenue, and
  despite the rapid development, the tech debt was kept on sustainable levels,
  so this one-off project is a good foundation for an actual product.
- However, it became pretty stressful to effectively defend the developer team
  from external scope changes and unnecessary overload, which caused an
  unresolved disagreement between the (now former) Product Owner and me and
  made me resign from this team.
- _Keywords_: Clean architecture, Architecture design, Java, Python, XML, XSLT,
  Ubuntu, systemd, V2X

## Experience

### Stealth-stage trading desk
`March 2023 - present`
__Founder__, London, United Kingdom

- \[see above, in the highlighted section\]

### Radix DLT

`September 2022 - March 2023`
__Senior Rust Engineer__, London, United Kingdom

- Mission: operate and improve a network of Radix validators
- My primary focus at Radix was improving the number of processed transactions
  by the validator nodes each second. These required increasing the
  observability by exporting tracing information to Grafana (and not exceeding
  our budget), seeking and dividing mutexes cautiously.
- I paved the way for generating flame graphs based on the perf counters, with
  all the available debug information across a weird mixture of Java and Rust
  stack trace, which highlighted many of our frequently hit bottlenecks.

### Prima Assicurazioni 

`May 2022 - August 2022`
__Rust Engineer__, Milan, Italy (remote)

- Mission: spin up an insurance selling platform in Spain
- The main challenges were integrating with third-party data providers, as well
  as a forced usage of a custom flavour of CQRS/event sourcing.
- Unfortunately, our partnership had to come to a premature end, as the company
  could not facilitate my eventual relocation to the United Kingdom.
- _Keywords_: Rust, CQRS/ES, Elm

### Commsignia

`April 2021 - April 2022`
__DevOps Engineer__, Budapest, Hungary

- Mission: there was no dedicated owner of the engineering supporting systems
  (e.g. GitLab, archives, object storages), and I wanted to fill this gap and
  improve overall engineering effectiveness.
- The other developers were happy and relieved with this transition, as
  previously accumulated tech debt could be paid back.
- Example: I have achieved a 90-95% cache hit rate for the main builds,
  halving the CI runtime immediately.
- Example: While no budget was planned for 2021, I have increased the capacity
  by repurposing old desktop machines to GitLab-CI runners.
- _Keywords_: DevOps, Gitlab, CI, ccache, S3, MinIO

`August 2020 - April 2021`
__Software Architect__, Budapest, Hungary

- \[see above, in the highlighted section\]

`March 2020 - July 2020`
__Senior Embedded Developer__, Budapest, Hungary

- This part was onboarding to the Vehicle-to-anything (V2x) industry
  and returning to embedded C development.
- Worked on a V2x - MQTT integration for a Smart City deployment.
- (This chapter was rather short, as a more impactful role had to be filled urgently.)
- _Keywords_: Embedded C, gdb, V2X, MQTT

### IBM Budapest Lab

`September 2018 - March 2020`
__Cloud Service Developer (band 7)__, Budapest, Hungary
- Mission: we have developed a service which uses IBM Watson to create
  transcriptions to a live video stream and enrich uploaded videos.
- This service was written mainly in Go(lang), and our team operated it in
  multiple Kubernetes clusters on IBM Cloud.
- Example: Before I joined the team, they struggled with Travis CI, it ran for
  hours and failed every second run. Fortunately, I could introduce some
  checkpoints, reducing the time it takes to under 40 minutes.
- Example: the monorepo created tens of Docker images as an artefact,
  but we could not detect which images had been changed between releases
  because of the massively intertwined repository. I have separated this
  repository into 30ish repositories without causing significant overhead to
  the other developers, based on generated dependency graph between the go
  packages; the new repositories created at most a single artefact, making 
  tracing changes straightforward.
- Conclusion: Eventually, we realized that the first architecture of the Video Enrichment
  product became hard to develop any further, and I was selected for the team
  that created the new pipes-and-filters like architecture for the new
  Video Enrichment Platform. Unfortunately, the relief efforts and the redesign were
  too late. The product was eventually switched to maintanence-only mode.
- _Keywords_: Go(lang), Kubernetes, DevOps, Docker, Travis CI, Terraform

### Balabit (later aquired by One Identity)
`August 2016 - September 2018`
__Platform Engineer__, Budapest, Hungary

- Mission: Balabit had two appliances as a product, and a new team has formed
  to unify the underlying operating systems. We became the owner and developer
  of this layer.
- This was a valuable experience with unattended low-level scripts (e.g.
  repartitioning a disk during an upgrade process) where fixing mistakes would
  be rather costly.
- Example: I have made run Shell Control Box available in AWS and GCE, where
  these cloud providers made it deliberately hard to run our own Linux
  distribution.

`February 2015 - August 2016`
__Software Engineer Trainee__, Budapest, Hungary
- Worked on syslog-ng, my first experience with async I/O in C.

### Nokia Networks
`September 2014 - January 2015`
__Research Assistant__, Budapest, Hungary
- Worked on pedestrian movement modelling for 5G network simulations.

### Sophos
`July 2013 - September 2014`
__Junior Developer__, Budapest, Hungary
- Worked on some e-mail filtering appliances written in Perl.

## Education

`Grad. 2017`
__B.Sc. in Software Engineering__, Budapest University of Technology and Economics 

## Tidbits
- Personal best lifts: 130 kg squat, 100 kg bench press, 170 kg deadlift
- Favourite editor: LunarVim
