<template>
  <div class="Job" id="Jobs">
    <h2 class="Title"> JOBS</h2>

    <div class="row Vacancies">
    <!-- Frontend -->
      <div class="col-md-4">
        <a href="https://careers.adobe.com/us/en/job/R145407/Engineering-Manager" target="_blank">
            <h3 class="Vacancy">Engineering Manager</h3>
            <p class="Company">Adobe Armenia</p>
        </a>
      </div>
    <!-- Backend -->
      <div class="col-md-4">
        <a href="https://careers.adobe.com/us/en/job/R144037/Sr-Product-Manager" target="_blank">
            <h3 class="Vacancy">Sr. Product Manager</h3>
            <p class="Company">Adobe Armenia</p>
        </a>
      </div>
    <!-- Fullstack, Mobile & More -->
      <!-- <div class="col-md-4">
        <a href="https://www.simplytechnologies.net/careers/javascript-developer" target="_blank">
            <h3 class="Vacancy">Full-Stack JS Developer</h3>
            <p class="Company">Simply Technologies</p>
        </a>
      </div> -->
    </div>

  </div>
</template>

<script>
export default {

};
</script>

<style scoped lang="scss">
.Job {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  flex-direction: column;
  padding: 100px 0;
}

a {
  color: #4bb463;
  font-weight: bold;
}


.Title {
  text-transform: uppercase;
  text-align: center;
  margin-bottom: 50px;
  color: black;
}

.Vacancy {
  color: #333;
}

.Company {
  margin-bottom: 1.5em;
}

.Vacancies {
  width: 65%;
}

@media (max-width: 768px) {
  .Job {
    padding: 50px 0 20px;
  }

  .Vacancies {
    width: 100%;
  }

  .Title {
    font-size: 1.6em;
    margin-bottom: 20px;
  }

  .Vacancy {
    font-size: 1em;
  }
}
</style>
