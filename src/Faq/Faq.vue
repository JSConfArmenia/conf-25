<template>
  <div class="Faq" id="Faq">
    <h2 class="Title"> FREQUENTLY ASKED QUESTIONS</h2>

    <div class="row Answers">
      <div class="col-md-6">
        <h3 class="Question">What is JavaScript Conference Armenia?</h3>
        <p class="Answer">
          JS Conf Armenia is a premier event for software engineers, hosted annually in Yerevan, Armenia. It features esteemed speakers who share their insights with JavaScript developers of varying expertise levels.
        </p>
        <h3 class="Question">When and where is it going to take place?</h3>
        <p class="Answer">
          JSConfAM25 is going to be held at Armenak Armeniakyan 2/4, Synergy Business Center.
        </p>
        <h3 class="Question">What is the conference language?</h3>
        <p class="Answer">
          All JSConfAM25 talks will be in Armenian.
        </p>
        <!-- <h3 class="Question">Who are the speakers?</h3>
        <p class="Answer">
          To see the line up, please,
          <a href="#Speakers">click here</a>.
        </p> -->
        <!-- <h3 class="Question">What are the talk topics?</h3>
        <p class="Answer">
          To see the conf agenda, please,
          <a href="#Agenda">click here</a>.
        </p> -->
        <h3 class="Question">Who are the organizers? </h3>
        <p class="Answer">
          To see JS Conf Armenia team, please,
          <a href="#Team">click here</a>.
        </p>
        <!-- <h3 class="Question">Who supports JS Conf Armenia?</h3>
        <p class="Answer">
          Armenian and regional tech companies who value community events and experience exchange activities.
          To learn about our sponsors and partners, please,
          <a href="#Sponsors">click here</a>.
        </p> -->
      </div>

      <div class="col-md-6">
        <h3 class="Question">How to participate?</h3>
        <p class="Answer">
          The sale of the tickets hasn't started yet.
          <!-- The registration has already started. To get your tickets, please,
          <a href="https://fienta.com/js-conf-armenia-2024">click here</a>. -->
        </p>
        <!-- <h3 class="Question">How much is the entry-ticket?</h3>
        <p class="Answer">
          The ticket price is $16.23.
        </p> -->
        <!-- <h3 class="Question">When is the deadline for registration?</h3>
        <p class="Answer">
          There is no deadline for buying ticket but the sooner you get it you cheaper it will cost.
        </p>
        <h3 class="Question">How can I help the team?</h3>
        <p class="Answer">
        This year we are not accepting volunteer applications but you can share the word about the conf. It will be appreciated.
        </p> -->
        <h3 class="Question">How to become a speaker?</h3>
        <p class="Answer">
          The speaker application opening soon.
        </p>
        <h3 class="Question">How to become a sponsor?</h3>
        <p class="Answer">
          <!-- Sign up <a href="https://bit.ly/3qRPuOm">here</a> for conference news and sponsorship opportunities in 2024. -->
          The sponsorship application opening soon.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {

};
</script>

<style scoped lang="scss">
.Faq {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  flex-direction: column;
  padding: 100px 0;
}

a {
  color: #FF00AA;
  font-weight: bold;
}


.Title {
  text-transform: uppercase;
  text-align: center;
  margin-bottom: 50px;
  color: #FF00AA;
}

.Question {
  color: #333;
}

.Answer {
  margin-bottom: 1.5em;
}

.Answers {
  width: 65%;
}

@media (max-width: 768px) {
  .Faq {
    padding: 50px 0 20px;
  }

  .Answers {
    width: 100%;
  }

  .Title {
    font-size: 32px;
    margin-bottom: 20px;
  }

  .Question {
    font-size: 1em;
  }
}
</style>
