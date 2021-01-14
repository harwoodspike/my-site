<template>
  <div class="h-screen w-full mx-auto max-w-3xl p-8">
    <h1 class="text-3xl">{{ title }}</h1>
    <p>Contact Info omitted, please use contact form</p>

    <Card class="my-6">
      <h2 class="text-2xl underline mb-4">Summary</h2>
      <div>{{ summary }}</div>
    </Card>

    <Card class="my-6">
      <h2 class="text-2xl underline mb-4">Work Experience</h2>
      <div v-for="job in work" :key="job.id">
        {{ job.name }} - {{ job.position }}
      </div>
    </Card>

    <Card class="my-6">
      <h2 class="text-2xl underline mb-4">Education</h2>
      <div v-for="school in education" :key="school.id">
        {{ school.name }} - {{ school.degree }}
      </div>
    </Card>

    <Card class="my-6">
      <h2 class="text-2xl underline mb-4">Skills</h2>
      <div v-for="skill in skills" :key="skill.id">
        {{ skill.name }} - {{ skill.level }}
      </div>
    </Card>
  </div>
</template>

<script>
export default {
  data: () => ({
    title: "Joshua Harwood",
    summary:
      "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt.",
    work: [
      { id: 1, name: "DSU", position: "CIT Lab Tech" },
      { id: 2, name: "Fusioncore", position: "Developer" },
      {
        id: 2,
        name: "Innovation Simple",
        position:
          "Website Developer, Server Admin, Network Admin, Backend Developer",
      },
    ],
    education: [
      { id: 1, name: "Dixie High School", degree: "Diploma" },
      { id: 2, name: "Dixie State University", degree: "Associate of Science" },
      {
        id: 3,
        name: "ITT Tech",
        degree:
          "Associate of Applied Science in Information Systems Administration",
      },
    ],
    skills: [
      { id: 1, name: "(X)HTML", level: 90 },
      { id: 2, name: "CSS", level: 75 },
      { id: 3, name: "JavaScript", level: 85 },
    ],
  }),
  created() {
    // fetch resume data
  },
};
</script>

<style></style>
