<script setup lang="ts">
</script>

<template>
  <main>
    <!-- Hero -->
    <section class="hero">
      <h1 class="hero__title">Kubernetes Demystified<br>A guide for a non-techie</h1>
      <img class="hero__lines" src="@/assets/images/lines.svg" alt="Kubernetes" />

      <div class="hero__card">
        <h2 class="hero__card__title">WHAT is K8S </h2>
        <p>Welcome to the world of Kubernetes, or K8s—a powerful open-source platform that might seem complex at first but is here to simplify how modern software is managed. Think of Kubernetes as the backbone of cloud computing, designed to keep applications running smoothly, scale effortlessly with demand, and handle unexpected challenges.</p>
        <p>We know Kubernetes can feel overwhelming, but don’t worry—the goal is to break it down into clear, simple ideas so you can see how it all comes together. We’ll explore a few key concepts, when and why Kubernetes (K8s) was created, and how it powers the modern world—using Netflix as a real-world example. Let’s dive in and make the cloud a little less cloudy!</p>
      </div>

      <img class="hero__card__image" src="@/assets/images/SUSE_Illustration_Rancher 1.svg" alt="Kubernetes" />
    </section>

    <!-- Timeline -->
    <section class="timeline">
      <h1 class="timeline__title">Timeline</h1>
      <ul class="timeline__list">
        <li><strong>1980s</strong>Businesses started generating and storing large amounts of digital data.</li>
        <li><strong>2000s</strong>AWS, Azure, and Google offered on-demand cloud computing resources.</li>
        <li><strong>2010s</strong>Lightweight containers invented to run apps consistently across environments.</li>
        <li><strong>2014</strong>Google launched K8s technology to automate the management of containers.</li>
        <li><strong>2014</strong>Rancher Labs was started to simplify container management.</li>
        <li><strong>2016</strong>Rancher adopted K8s as the orchestrator for managing containers.</li>
        <li><strong>2018</strong>The first enterprise-grade platform Rancher 2.0 Launched.</li>
        <li><strong>2020</strong>Rancher acquired by SUSE, a leading open-source innovator.</li>
      </ul>
      <img class="timeline__image" src="@/assets/images/SUSE_Illustration_Train 1.svg" alt="Kubernetes" />
    </section>

    <!-- Use Cases -->
    <section class="cases">
      <h1 class="cases__title">Most Common Use Cases of Kubernetes</h1>

      <div class="cases__cards">
        <div class="cases__card">
          <div class="cases__card__header">Deployment & Scaling</div>
          <div class="cases__card__body">
            Automating the deployment and scaling of applications based on demand.<br>
            <strong>E.g.:</strong> E-commerce platforms scaling during Black Friday sales.
          </div>
        </div>

        <div class="cases__card">
          <div class="cases__card__header">Microservices Management</div>
          <div class="cases__card__body">
            Orchestrating multiple services that work together to form a complete application.<br>
            <strong>E.g.:</strong> Netflix uses K8s to manage services like recommendations, video playback, and search.
          </div>
        </div>

        <div class="cases__card">
          <div class="cases__card__header">Continuous Integration & Delivery</div>
          <div class="cases__card__body">
            Automating testing and deployment pipelines for faster development cycles.<br>
            <strong>E.g.:</strong> Startups releasing new versions of their apps several times a day.
          </div>
        </div>

        <div class="cases__card">
          <div class="cases__card__header">Edge Computing</div>
          <div class="cases__card__body">
            Running applications at the network's edge, closer to users or devices, for lower latency.<br>
            <strong>E.g.:</strong> Retail chains managing inventory systems locally in stores using K8s distributions like k3s.
          </div>
        </div>

        <div class="cases__card">
          <div class="cases__card__header">Disaster Recovery</div>
          <div class="cases__card__body">
            Ensuring applications remain online even during system failures.<br>
            <strong>E.g.:</strong> Media streaming platforms like Spotify ensuring uninterrupted service during server outages.
          </div>
        </div>

        <div class="cases__card">
          <div class="cases__card__header">Dev/Test Environments</div>
          <div class="cases__card__body">
            Quickly spinning up isolated environments for developers to test their code.<br>
            <strong>E.g.:</strong> Software teams using K8s to mimic production environments for realistic testing.
          </div>
        </div>
      </div>
    </section>

    <!-- Key Problems -->
    <section class="problems">
      <h2>What it does</h2>
      <h1>Key Problems Solved by Kubernetes</h1>
      <ul>
        <li>
          <header>Reliability</header>
          <section>Apps stay online, even if something goes wrong.</section>
          <img src="@/assets/images/SLES ARM.svg" alt="">
        </li>
        <li>
          <header>Scalability</header>
          <section>Handle millions of users effortlessly.</section>
          <img src="@/assets/images/SLE Rea Time.svg" alt="">
        </li>
        <li>
          <header>Failures Recovery</header>
          <section>Ensures that applications can return to their most recent state without data loss.</section>
          <img src="@/assets/images/BCL 1.svg" alt="">
        </li>
      </ul>
    </section>

    <!-- Core Concepts -->
    <section class="concepts">
      <h1>The Core Concepts of Kubernetes: Containers, Pods, and Clusters</h1>
      <div class="card">
        <div class="card__title">Containers: The Building Blocks</div>
        <div class="card__content">
          <p>In Kubernetes, each feature of an application is packaged in a container. Containers include everything the feature needs—code, libraries, and configurations—to run consistently across different environments. For example, a shipping app’s features like tracking packages or generating shipping labels would each be packaged in separate containers.</p>
          <p><strong>Analogy:</strong> Think of containers as individual packages in a postal system. Each package is carefully packed with everything required for its specific destination, ensuring it can be handled independently without affecting other shipments.</p>
        </div>
        <img src="@/assets/images/Illustration_containers.svg" alt="Containers">
      </div>

      <div class="card">
        <div class="card__title">Pods: The Team Players</div>
        <div class="card__content">
          <p>Kubernetes groups containers into pods, which are the smallest deployable units in the system. A pod can consist of one or more containers that work together to perform a task, sharing resources like storage and network access. For instance, in the shipping app, a pod might handle processing a shipment, with one container managing the label and another updating tracking information.</p>
          <p><strong>Analogy:</strong> A pod is like a small team in a post office. One worker scans the package, another updates the tracking system, and another prepares the route—all collaborating to ensure the shipment is processed smoothly.</p>
        </div>
        <img src="@/assets/images/Illustration_pods.svg" alt="Pods">
      </div>

      <div class="card">
        <div class="card__title">Clusters: The Workforce</div>
        <div class="card__content">
          <p>Kubernetes runs applications on clusters, which are groups of machines (nodes) working together. Clusters distribute workloads to ensure high availability and scalability. For example, the shipping app might run on multiple servers in different locations, allowing tasks to be handled where they are needed most.</p>
          <p><strong>Analogy:</strong> A cluster is like a fleet of delivery drivers across multiple cities. If one driver is unavailable in a region, another driver steps in to ensure packages are delivered without delay, keeping the service reliable and efficient.</p>
        </div>
        <img src="@/assets/images/Illustration_clusters.svg" alt="Clusters">
      </div>
    </section>

    <!-- Real-World Example -->
    <section class="example">
      <img src="@/assets/images/SVG.svg" alt="Clusters">
    </section>

    <!-- Netflix -->
    <section class="netflix">
      <h1>What happens inside Kubernetes while you are watching a Netflix show?</h1>
      <div>
        <p>While you’re watching a Netflix show, Kubernetes orchestrates the entire backend system to ensure a seamless experience. Your request is handled by the API Server in the nearest cluster (e.g. your region), which directs tasks to Worker Nodes. </p>
        <p>The Scheduler assigns resources efficiently, while the Controller Manager ensures services like streaming and recommendations are always running. Etcd keeps track of the cluster’s state, ensuring data consistency. </p>
        <p>On Worker Nodes, Kubelet ensures that containers run as instructed, delivering video playback, caching content, and updating recommendations. All of this happens automatically, so you can watch without interruptions.</p>
      </div>
    </section>

    <!-- Conclusion -->
    <section class="conclusion">
      <p>The next time you stream your favourite show, remember that Kubernetes is behind the scenes, working tirelessly to ensure your seamless experience.</p>
      <img src="@/assets/images/suse_hackweek_24_light_background 1.svg" alt="">
    </section>
  </main>
</template>

<style scoped>
main {
  display: flex;
  width: 1440px;
  padding: 0px 290px;
  flex-direction: column;
  align-items: center;
  gap: 100px;
}

img {
  max-width: 100%;
}

.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 80px;
  padding-top: 300px;
}

.hero__title {
  color: var(--Persimmon, #FE7C3F);
  font-family: SUSE;
  font-size: 72px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

.hero__lines {
  display: flex;
  width: 824px;
  height: 109.85px;
  justify-content: center;
  align-items: center;
}

.hero__card {
  display: flex;
  padding: 32px;
  box-sizing: content-box;
  flex-direction: column;
  align-items: flex-start;
  gap: 32px;
  align-self: stretch;
  border-radius: 20px;
  background: var(--Mint-700, #01564A);
}

.hero__card__title {
  color: var(--Persimmon, #FE7C3F);
  font-variant-numeric: lining-nums tabular-nums;
  font-feature-settings: 'liga' off, 'clig' off;
  font-family: SUSE;
  font-size: 20px;
  font-style: normal;
  font-weight: 700;
  line-height: 30px; /* 150% */
  letter-spacing: 1.5px;
  text-transform: uppercase;
}

.hero__card__image {
  width: 664px;
  height: 664px;
}

.timeline {
  display: flex;
  width: 1300px;
  flex-direction: column;
  align-items: flex-start;
  gap: 27px;
  padding: 24px;

  background: var(--Mint-800, #0C322C);
}

.timeline__title {
  color: var(--Waterhole-100, #E6EDFE);
  font-family: SUSE;
  font-size: 26px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}

.timeline__list {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 16px;
  padding: 0px;
}

.timeline__list li {
  display: flex;
  width: 140px;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 16px;
}

.timeline__list  strong {
  color: var(--Persimmon-500, #FF5A2B);
  text-align: right;
  font-family: SUSE;
  font-size: 16px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}

.timeline__image {
  margin: -39px -42px;
  margin-top: 24px;
}

.cases__title {
  color: var(--Jungle-100, #EAFAF4);
  text-align: center;
  margin-bottom: 40px;

  /* h2 */
  font-family: SUSE;
  font-size: 48px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

.cases__cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}

.cases__card {
  display: flex;
  padding: 32px;
  flex-direction: column;
  align-items: flex-start;
  gap: 32px;
  flex: 1 0 0;
  align-self: stretch;

  border-radius: 20px;
  border: 4px solid var(--Mint-400, #38D5B4);
  background: var(--Mint-800, #0C322C);
}

.cases__card__header {
  color: var(--Mint-400, #38D5B4);
  font-family: SUSE;
  font-size: 24px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}
.cases__card__body {
  color: var(--White, #FFF);
  /* cards */
  font-family: SUSE;
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px; /* 133.333% */
}
</style>
