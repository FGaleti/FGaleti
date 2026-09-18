<h1 align="center">Felipe Galeti Gôngora</h1>

<h3 align="center">
  DevOps Engineer | Automation Pipelines, Kubernetes Operations & Cloud Environments
</h3>

<p align="center">
  <img
    src="https://img.shields.io/badge/Focus-DevOps%20%26%20SRE-0A66C2?style=flat-square"
    alt="DevOps and SRE"
  />
  <img
    src="https://img.shields.io/badge/Automation-Pipelines%20%26%20CI%2FCD-6A1B9A?style=flat-square"
    alt="Automation Pipelines and CI/CD"
  />
  <img
    src="https://img.shields.io/badge/Kubernetes-Cluster%20Operations-326CE5?style=flat-square&logo=kubernetes&logoColor=white"
    alt="Kubernetes Cluster Operations"
  />
  <img
    src="https://img.shields.io/badge/Cloud-AWS%20%26%20Observability-FF9900?style=flat-square"
    alt="Cloud and Observability"
  />
</p>

<p align="center">
  DevOps Engineer focused on automation pipelines, Kubernetes cluster
  operations and sustainment, cloud environments, and end-to-end
  observability for production systems.
</p>

<p align="center">
  I turn fragile, manual deploys into automated pipelines with real
  health checks, keep Kubernetes and cloud environments running reliably
  day to day, and turn blind infrastructure into observable systems
  with actionable alerts.
</p>

<p align="center">
  Software Engineering undergraduate at UniCesumar.
</p>

<h2 id="about-me">About Me</h2>

I work as a **DevOps Engineer** on infrastructure and reliability, currently
on the Development team at **liveSEO**, where I own everything from
automation pipelines and Kubernetes cluster operations to cloud
infrastructure, observability, and production incident response.

My day-to-day mixes **deployment automation** (blue/green rollouts with real
health checks and automatic rollback), **Kubernetes and cloud environment
sustainment** on AWS, **observability platform engineering** (Grafana
Cloud stack: Loki, Mimir, Tempo, Alloy, and Grafana Faro for frontend RUM),
and **hands-on root cause analysis** on hosts running Docker, Nginx, Redis,
and Postgres in production.

I care about replacing manual, error-prone operational steps with pipelines
and dashboards that fail loudly, roll back safely, and explain themselves,
so incidents get caught by an alert instead of by a user.

### Main technical objectives

- Ship deployments through automated pipelines with real health checks and rollback, not "green build, cross your fingers";
- Operate and sustain Kubernetes clusters and cloud environments with reliability and cost-efficiency in mind;
- Increase the visibility and reliability of critical production environments;
- Automate repetitive and error-prone operational processes;
- Reduce incident detection and resolution time through observability and alerting;
- Integrate infrastructure platforms through secure REST APIs;
- Build reusable and maintainable monitoring solutions;
- Apply version control, RCA discipline, and continuous improvement practices to infrastructure;
- Apply information security and LGPD principles to infrastructure processes.

---

<h2 id="recent-highlights">Recent DevOps Highlights: By the Numbers</h2>

<p>A few things I've recently designed, built, or fixed in production and staging environments, with real impact behind each one:</p>

- **Blue/green deployment pipeline with automated rollback:** designed and shipped a deployment pipeline for a containerized production API with real health checks, a bake-time validation window, and automatic rollback on failure. The winning slot is recreated and fully health-verified in **under 30 seconds**, and the mechanism was validated end-to-end in **both success and induced-failure scenarios** before going live.
- **Observability cost & cardinality optimization:** audited a multi-host Grafana Cloud account running at **~79% of its metrics quota**, traced the overage to unnecessary system-level cAdvisor (cgroup) collection instead of real container metrics, and shipped a fix **projected to reclaim ~42% of the total quota**, without touching a single existing dashboard or alert.
- **Grafana Cloud observability platform:** built and rolled out logs, metrics, and traces (Loki, Mimir, Tempo, Grafana Alloy) across **production/staging hosts** on AWS with auto-discovery dashboards and alert routing tuned to cut noisy, generic alerts, plus **Grafana Faro (RUM)** instrumentation for end-to-end frontend observability.
- **Production Redis OOM root cause & fix:** root-caused a Redis container being killed by the OOM killer roughly **every 30 minutes**, tracing it to **~56,000 unbounded session keys (75–190 KB each, ~4.2 GB total)** with no memory ceiling; fixed with a persisted `maxmemory` configuration, stabilizing uptime with **zero data loss** on session data that couldn't be evicted.
- **Distributed tracing rollout:** instrumented a Node.js/TypeScript service end-to-end with OpenTelemetry auto-instrumentation (app → Alloy → Grafana Cloud Tempo), including trace filtering to keep health-check noise out of the pipeline.
- **CI/CD false-positive investigation:** diagnosed a deploy pipeline reporting a **green build in ~16 seconds on every run** while silently failing to update the running container in production, tracing it to a non-blocking remote command inside the deploy step.
- **Container CPU root cause analysis:** root-caused a workload spiking to **~100% of a CPU core every 30 seconds** in a Celery/Airflow environment, tracing it to a container healthcheck reloading the entire application on every run, diagnosed with **zero changes** to the live environment.

---

<h2 id="areas-of-expertise">Areas of Expertise</h2>

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>Automation Pipelines & Kubernetes/Cloud Ops</h3>
      <p>
        Design and hardening of deployment pipelines (GitHub Actions,
        container-based deploys), including blue/green rollouts, health
        checks, bake-time validation, and automatic rollback, plus day-to-day
        operation and sustainment of Kubernetes clusters and cloud (AWS)
        environments.
      </p>
    </td>
    <td width="50%" valign="top">
      <h3>Observability & Monitoring</h3>
      <p>
        Deployment and maintenance of monitoring solutions using Grafana Cloud
        (Loki, Mimir, Tempo, Alloy) and Zabbix, including custom dashboards,
        alerting, distributed tracing, and cardinality/cost optimization.
      </p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>Infrastructure Operations & RCA</h3>
      <p>
        Administration and troubleshooting of Linux, Windows, and AIX
        environments (Docker, Nginx, Redis, and Postgres in production),
        with a focus on root cause analysis over quick patches.
      </p>
    </td>
    <td width="50%" valign="top">
      <h3>Virtualization & Backup</h3>
      <p>
        Operation and monitoring of VMware and Hyper-V environments,
        including backup, replication, capacity, recovery, and protection
        routines with Veeam.
      </p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>API Integrations & Data</h3>
      <p>
        Integration of infrastructure platforms through REST APIs and
        operational data processing using SQL, PostgreSQL, SQLite,
        JavaScript, and scripting languages.
      </p>
    </td>
    <td width="50%" valign="top">
      <h3>Security & Compliance</h3>
      <p>
        Application of information security practices, access control,
        credential protection, operational traceability, and data protection
        principles aligned with LGPD.
      </p>
    </td>
  </tr>
</table>

---

<h2 id="devops-workflow">DevOps Workflow</h2>

<p align="center">
  <img
    src="https://img.shields.io/badge/Code-Development-0A66C2?style=for-the-badge&logo=visualstudiocode&logoColor=white"
    alt="Code"
  />
  &nbsp;➜&nbsp;
  <img
    src="https://img.shields.io/badge/Commit-Git-F05032?style=for-the-badge&logo=git&logoColor=white"
    alt="Commit"
  />
  &nbsp;➜&nbsp;
  <img
    src="https://img.shields.io/badge/CI-GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"
    alt="Continuous Integration"
  />
  &nbsp;➜&nbsp;
  <img
    src="https://img.shields.io/badge/Test-Health_Checks-2E7D32?style=for-the-badge&logo=checkmarx&logoColor=white"
    alt="Test and Health Checks"
  />
  &nbsp;➜&nbsp;
  <img
    src="https://img.shields.io/badge/Deploy-Blue%2FGreen-6A1B9A?style=for-the-badge"
    alt="Blue-Green Deployment"
  />
  &nbsp;➜&nbsp;
  <img
    src="https://img.shields.io/badge/Monitor-Observability-F46800?style=for-the-badge&logo=grafana&logoColor=white"
    alt="Monitoring and Observability"
  />
</p>

<p align="center">
  <strong>
    Automation as a standard. Observability as a foundation.
    Rollback as a safety net.
  </strong>
</p>

---

<h2 id="tech-stack">Tech Stack</h2>

<h3>CI/CD & Deployment</h3>

<p>
  <img
    alt="GitHub Actions"
    src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"
  />
  <img
    alt="Docker"
    src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"
  />
  <img
    alt="Nginx"
    src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white"
  />
  <img
    alt="Amazon ECR"
    src="https://img.shields.io/badge/Amazon_ECR-FF9900?style=for-the-badge&logo=amazonecs&logoColor=white"
  />
  <img
    alt="SSH"
    src="https://img.shields.io/badge/SSH-000000?style=for-the-badge&logo=gnubash&logoColor=white"
  />
</p>

<h3>Observability & Monitoring</h3>

<p>
  <img
    alt="Grafana"
    src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white"
  />
  <img
    alt="Prometheus"
    src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white"
  />
  <img
    alt="Loki"
    src="https://img.shields.io/badge/Loki-33B8FF?style=for-the-badge&logo=grafana&logoColor=white"
  />
  <img
    alt="Tempo"
    src="https://img.shields.io/badge/Tempo-8B45F6?style=for-the-badge&logo=grafana&logoColor=white"
  />
  <img
    alt="Mimir"
    src="https://img.shields.io/badge/Mimir-FFA300?style=for-the-badge&logo=grafana&logoColor=white"
  />
  <img
    alt="OpenTelemetry"
    src="https://img.shields.io/badge/OpenTelemetry-000000?style=for-the-badge&logo=opentelemetry&logoColor=white"
  />
  <img
    alt="Grafana Faro"
    src="https://img.shields.io/badge/Grafana_Faro_(RUM)-F46800?style=for-the-badge&logo=grafana&logoColor=white"
  />
  <img
    alt="Zabbix"
    src="https://img.shields.io/badge/Zabbix-CC0000?style=for-the-badge&logo=zabbix&logoColor=white"
  />
</p>

<h3>Infrastructure & Data Stores</h3>

<p>
  <img
    alt="Redis"
    src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white"
  />
  <img
    alt="PostgreSQL"
    src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"
  />
  <img
    alt="SQLite"
    src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white"
  />
  <img
    alt="Apache Airflow"
    src="https://img.shields.io/badge/Apache_Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white"
  />
</p>

<h3>Automation, Scripting & APIs</h3>

<p>
  <img
    alt="Python"
    src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"
  />
  <img
    alt="Shell Script"
    src="https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white"
  />
  <img
    alt="PowerShell"
    src="https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white"
  />
  <img
    alt="JavaScript"
    src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"
  />
  <img
    alt="RunDeck"
    src="https://img.shields.io/badge/RunDeck-D6373D?style=for-the-badge&logo=rundeck&logoColor=white"
  />
  <img
    alt="REST API"
    src="https://img.shields.io/badge/REST_API-005571?style=for-the-badge&logo=fastapi&logoColor=white"
  />
</p>

<h3>Operating Systems & Remote Administration</h3>

<p>
  <img
    alt="Linux"
    src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black"
  />
  <img
    alt="Windows"
    src="https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white"
  />
  <img
    alt="IBM AIX"
    src="https://img.shields.io/badge/IBM_AIX-052FAD?style=for-the-badge&logo=ibm&logoColor=white"
  />
  <img
    alt="RDP"
    src="https://img.shields.io/badge/RDP-0078D6?style=for-the-badge&logo=windows&logoColor=white"
  />
</p>

<h3>Virtualization & Backup</h3>

<p>
  <img
    alt="VMware"
    src="https://img.shields.io/badge/VMware-607078?style=for-the-badge&logo=vmware&logoColor=white"
  />
  <img
    alt="Hyper-V"
    src="https://img.shields.io/badge/Hyper--V-0078D6?style=for-the-badge&logo=windows&logoColor=white"
  />
  <img
    alt="Veeam"
    src="https://img.shields.io/badge/Veeam-00B336?style=for-the-badge&logo=veeam&logoColor=white"
  />
</p>

<h3>Containers & Orchestration</h3>

<p>
  <img
    alt="Docker"
    src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"
  />
  <img
    alt="Kubernetes"
    src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white"
  />
</p>

<h3>Infrastructure as Code & Configuration</h3>

<p>
  <img
    alt="Terraform"
    src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white"
  />
  <img
    alt="Ansible"
    src="https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white"
  />
  <img
    alt="YAML"
    src="https://img.shields.io/badge/YAML-CB171E?style=for-the-badge&logo=yaml&logoColor=white"
  />
</p>

<h3>Cloud Platforms</h3>

<p>
  <img
    alt="Amazon Web Services"
    src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white"
  />
  <img
    alt="Microsoft Azure"
    src="https://img.shields.io/badge/Microsoft_Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white"
  />
  <img
    alt="Oracle Cloud Infrastructure"
    src="https://img.shields.io/badge/Oracle_Cloud-F80000?style=for-the-badge&logo=oracle&logoColor=white"
  />
</p>

<h3>Security & Data Governance</h3>

<p>
  <img
    alt="Information Security"
    src="https://img.shields.io/badge/Information_Security-263238?style=for-the-badge&logo=securityscorecard&logoColor=white"
  />
  <img
    alt="LGPD Compliance"
    src="https://img.shields.io/badge/Compliance-LGPD-2E7D32?style=for-the-badge"
  />
</p>

> The technologies listed represent tools and platforms present in my
> professional, academic, laboratory, or project experience. My primary
> specialization is Infrastructure, CI/CD, Observability, and Operational
> Automation.

---

<h2 id="featured-projects">Featured Projects</h2>

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>
        <a href="https://github.com/FGaleti/Veeam-Backup-Replication-via-REST-API">
          Veeam Backup & Replication via REST API
        </a>
      </h3>
      <p>
        Advanced Zabbix template for monitoring Veeam Backup & Replication
        V12+ through its native REST API.
      </p>
      <p>
        Implements automatic discovery of Jobs, Proxies, and Repositories,
        including execution status, capacity metrics, availability, and
        dynamic API version routing.
      </p>
      <p>
        <strong>Technologies:</strong>
        Zabbix, JavaScript, REST API, Veeam, and YAML.
      </p>
    </td>
    <td width="50%" valign="top">
      <h3>
        <a href="https://github.com/FGaleti/MONITORING_IBM_STORAGES_API">
          IBM Storage Monitoring via REST API
        </a>
      </h3>
      <p>
        Observability solution for IBM storage systems using Zabbix and the
        native IBM Storage Virtualize REST API.
      </p>
      <p>
        Provides automatic discovery and monitoring of Pools, Volumes,
        Drives, Hosts, Enclosures, Canisters, and Power Supplies, including
        a ready-to-use Grafana dashboard.
      </p>
      <p>
        <strong>Technologies:</strong>
        Zabbix, Grafana, JavaScript, REST API, IBM Storage, and YAML.
      </p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>
        <a href="https://github.com/FGaleti/SCRIPT_VEEAM_v12-v13">
          Veeam V12/V13 Monitoring for Zabbix
        </a>
      </h3>
      <p>
        Monitoring integration between Veeam Backup & Replication and Zabbix
        using PowerShell and optimized XML exports.
      </p>
      <p>
        Reduces recurring queries against the Veeam environment while
        providing discovery and monitoring of Jobs, Virtual Machines,
        and Backup Repositories.
      </p>
      <p>
        <strong>Technologies:</strong>
        PowerShell, Zabbix, XML, and Veeam.
      </p>
    </td>
    <td width="50%" valign="top">
      <h3>
        <a href="https://github.com/FGaleti/LiveSeo-DevOps">
          Prática DevOps
        </a>
      </h3>
      <p>
        DevOps and infrastructure project focused on automation,
        observability, operational standardization, and continuous
        improvement practices.
      </p>
      <p>
        The repository demonstrates the application of DevOps concepts to
        infrastructure operations and technical process organization.
      </p>
      <p>
        <strong>Focus:</strong>
        Automation, infrastructure, monitoring, and operational reliability.
      </p>
    </td>
  </tr>
</table>

<p align="center">
  <a href="https://github.com/FGaleti?tab=repositories">
    <img
      src="https://img.shields.io/badge/View_All_Repositories-181717?style=for-the-badge&logo=github&logoColor=white"
      alt="View all repositories"
    />
  </a>
</p>

---

<h2 id="github-devops-activity">GitHub & DevOps Activity</h2>

<p align="center">
  Dynamic overview of my technical contributions, repositories,
  automation projects, and development activity.
</p>

<p align="center">
  <img
    src="https://raw.githubusercontent.com/FGaleti/FGaleti/main/metrics/profile-overview.svg?v=5"
    alt="GitHub profile overview"
    width="49%"
  />
</p>

<p align="center">
  <img
    src="https://raw.githubusercontent.com/FGaleti/FGaleti/main/metrics/contribution-calendar.svg?v=5"
    alt="GitHub contribution calendar"
    width="98%"
  />
</p>

<p align="center">
  <img
    src="https://raw.githubusercontent.com/FGaleti/FGaleti/main/metrics/devops-languages.svg?v=5"
    alt="Most used languages"
    width="49%"
  />
</p>

<p align="center">
  <sub>Metrics are updated automatically through GitHub Actions.</sub>
</p>

---

<h2 id="certifications">Certifications & Achievements</h2>

<p align="center">
  <img
    src="https://img.shields.io/badge/Zabbix-Certified_User-CC0000?style=for-the-badge&logo=zabbix&logoColor=white"
    alt="Zabbix Certified User"
  />
  <img
    src="https://img.shields.io/badge/LinuxTips-Uncomplicating_Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"
    alt="Uncomplicating Docker"
  />
  <img
    src="https://img.shields.io/badge/Linux_Foundation-LFS101%20%7C%20LFS151%20%7C%20LFS162-003778?style=for-the-badge&logo=linuxfoundation&logoColor=white"
    alt="Linux Foundation Certifications"
  />
  <img
    src="https://img.shields.io/badge/Zabbix_7.0-Application%20%26%20Network_Monitoring-CC0000?style=for-the-badge&logo=zabbix&logoColor=white"
    alt="Zabbix 7.0 Application and Network Monitoring"
  />
  <img
    src="https://img.shields.io/badge/Shell_Script-Linux_Automation-121011?style=for-the-badge&logo=gnubash&logoColor=white"
    alt="Shell Script and Linux Automation"
  />
  <img
    src="https://img.shields.io/badge/LGPD-Data_Protection-2E7D32?style=for-the-badge"
    alt="LGPD Data Protection"
  />
</p>

---

<h2 id="contact">Contact</h2>

<p align="center">
  <a href="https://www.linkedin.com/in/felipe-galeti-g%C3%B4ngora/">
    <img
      src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"
      alt="LinkedIn"
    />
  </a>
  <a href="mailto:fgaletigongora@gmail.com">
    <img
      src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"
      alt="Email"
    />
  </a>
  <a href="https://github.com/FGaleti">
    <img
      src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"
      alt="GitHub"
    />
  </a>
</p>

<br />

<p align="center">
  <strong>
    Building reliable, observable, secure, and automated infrastructure.
  </strong>
</p>

<p align="center">
  DevOps • CI/CD • Observability • Automation • Reliability
</p>
