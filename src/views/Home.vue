<template>
  <div class="home">
    <h2 class="title">
      Consigo maratonar
      <div class="container-multiselect">
        <multiselect
          v-model="selected"
          :options="options"
          selectLabel=""
          deselectLabel=""
          noResult="Nenhum título encontrado"
          placeholder="Game of Thrones"
          track-by="title"
          :option-height="34"
          :custom-label="customLabel"
          :show-labels="false"
        >
          <template slot="option" slot-scope="props">
            <div class="container-option">
              <img
                class="option__image"
                :src="
                  `https://image.tmdb.org/t/p/w500/${props.option.poster_path}`
                "
                alt="No Man’s Sky"
              />
              <div class="option__desc">
                <span class="option__title">{{ props.option.title }}</span
                ><span class="option__small">{{
                  props.option.release_date | releaseDate
                }}</span>
              </div>
            </div>
          </template>
        </multiselect>
      </div>
      em&nbsp;<span> 1 </span>&nbsp;
      <div class="color-primary align-flex-start">
        semana
        <div class="controls">
          <img src="@/assets/arrow_drop_up.svg" alt="Up" class="img-icon" />
          <img src="@/assets/arrow_drop_down.svg" alt="Down" class="img-icon" />
        </div>
      </div>
      ?
    </h2>
  </div>
</template>

<script>
import Multiselect from "vue-multiselect";
export default {
  name: "Home",
  components: { Multiselect },
  data() {
    return {
      selected: null,
      options: [
        {
          adult: false,
          backdrop_path: "/c7Mjuip0jfHLY7x8ZSEriRj45cu.jpg",
          genre_ids: [12, 28],
          id: 85,
          original_language: "en",
          original_title: "Raiders of the Lost Ark",
          overview:
            "When Dr. Indiana Jones – the tweed-suited professor who just happens to be a celebrated archaeologist – is hired by the government to locate the legendary Ark of the Covenant, he finds himself up against the entire Nazi regime.",
          popularity: 59.393,
          poster_path: "/awUGN7ZCNq2EUTdpVaHDX23anOZ.jpg",
          release_date: "1981-06-12",
          title: "Raiders of the Lost Ark",
          video: false,
          vote_average: 7.9,
          vote_count: 9159,
        },
        {
          adult: false,
          backdrop_path: "/vwkJChYb9dBcuds98Se4oHIcbnw.jpg",
          genre_ids: [18, 9648, 53, 36],
          id: 567970,
          original_language: "en",
          original_title: "Lost Girls",
          overview:
            "When Mari Gilbert's daughter disappears, police inaction drives her own investigation into the gated Long Island community where Shannan was last seen. Her search brings attention to over a dozen murdered sex workers.",
          popularity: 17.659,
          poster_path: "/pDas4DwURlRzjD9xEhSdtkcl1ZV.jpg",
          release_date: "2020-01-28",
          title: "Lost Girls",
          video: false,
          vote_average: 6.1,
          vote_count: 482,
        },
        {
          adult: false,
          backdrop_path: "/qyAH7xkrgYCGPbaFV29C82Hngum.jpg",
          genre_ids: [12, 18, 36],
          id: 314095,
          original_language: "en",
          original_title: "The Lost City of Z",
          overview:
            "A true-life drama in the 1920s, centering on British explorer Col. Percy Fawcett, who discovered evidence of a previously unknown, advanced civilization in the Amazon and disappeared whilst searching for it.",
          popularity: 56.052,
          poster_path: "/ik3ebv7J18fs6cHkmu91oxz7EGt.jpg",
          release_date: "2017-03-15",
          title: "The Lost City of Z",
          video: false,
          vote_average: 6.3,
          vote_count: 2121,
        },
        {
          adult: false,
          backdrop_path: "/ltt9yiCGmCQZunmxtkhtPxzmDzx.jpg",
          genre_ids: [12, 35, 10751],
          id: 499701,
          original_language: "en",
          original_title: "Dora and the Lost City of Gold",
          overview:
            "Dora, a girl who has spent most of her life exploring the jungle with her parents, now must navigate her most dangerous adventure yet: high school. Always the explorer, Dora quickly finds herself leading Boots (her best friend, a monkey), Diego, and a rag tag group of teens on an adventure to save her parents and solve the impossible mystery behind a lost Inca civilization.",
          popularity: 57.64,
          poster_path: "/xvYCZ740XvngXK0FNeSNVTJJJ5v.jpg",
          release_date: "2019-08-08",
          title: "Dora and the Lost City of Gold",
          video: false,
          vote_average: 6.8,
          vote_count: 1229,
        },
        {
          adult: false,
          backdrop_path: "/AeMtzbw7shxtLvwKKqeITabpTrD.jpg",
          genre_ids: [10751, 12, 16, 35],
          id: 137116,
          original_language: "en",
          original_title: "Smurfs: The Lost Village",
          overview:
            "In this fully animated, all-new take on the Smurfs, a mysterious map sets Smurfette and her friends Brainy, Clumsy and Hefty on an exciting race through the Forbidden Forest leading to the discovery of the biggest secret in Smurf history.",
          popularity: 33.793,
          poster_path: "/diYAZ6CKUuRAqLYMB2AyVutEFm0.jpg",
          release_date: "2017-03-23",
          title: "Smurfs: The Lost Village",
          video: false,
          vote_average: 6.3,
          vote_count: 1085,
        },
        {
          adult: false,
          backdrop_path: "/5v3Iubz9lkZwMEG17j0RHPLcwvx.jpg",
          genre_ids: [18, 53, 9648],
          id: 638,
          original_language: "en",
          original_title: "Lost Highway",
          overview:
            "A tormented jazz musician finds himself lost in an enigmatic story involving murder, surveillance, gangsters, doppelgangers, and an impossible transformation inside a prison cell.",
          popularity: 20.294,
          poster_path: "/5POhfNeFPIi4VUNwCTaK85sh98r.jpg",
          release_date: "1997-01-15",
          title: "Lost Highway",
          video: false,
          vote_average: 7.6,
          vote_count: 1724,
        },
        {
          adult: false,
          backdrop_path: "/fEolr0bwBR7m0sHSJC8u8grnhBv.jpg",
          genre_ids: [35, 18, 10749],
          id: 153,
          original_language: "en",
          original_title: "Lost in Translation",
          overview:
            "Two lost souls visiting Tokyo -- the young, neglected wife of a photographer and a washed-up movie star shooting a TV commercial -- find an odd solace and pensive freedom to be real in each other's company, away from their lives in America.",
          popularity: 15.123,
          poster_path: "/wkSzJs7oMf8MIr9CQVICsvRfwA7.jpg",
          release_date: "2003-09-18",
          title: "Lost in Translation",
          video: false,
          vote_average: 7.4,
          vote_count: 5384,
        },
        {
          adult: false,
          backdrop_path: "/giaqkJawiez0jnXMdm9OwSmJhPd.jpg",
          genre_ids: [12, 35, 878, 10751],
          id: 18162,
          original_language: "en",
          original_title: "Land of the Lost",
          overview:
            "On his latest expedition, Dr. Rick Marshall is sucked into a space-time vortex alongside his research assistant and a redneck survivalist. In this alternate universe, the trio make friends with a primate named Chaka, their only ally in a world full of dinosaurs and other fantastic creatures.",
          popularity: 17.317,
          poster_path: "/y1FBpV3qXT1yOUR2tRUWKtpo9Oy.jpg",
          release_date: "2009-06-05",
          title: "Land of the Lost",
          video: false,
          vote_average: 5.4,
          vote_count: 925,
        },
        {
          adult: false,
          backdrop_path: "/igHPYHUDVNQKfixdrUiu1Jgk2Ko.jpg",
          genre_ids: [16, 10751, 12, 14],
          id: 25475,
          original_language: "en",
          original_title: "Tinker Bell and the Lost Treasure",
          overview:
            "A blue harvest moon will rise, allowing the fairies to use a precious moonstone to restore the Pixie Dust Tree, the source of all their magic. But when Tinker Bell accidentally puts all of Pixie Hollow in jeopardy, she must venture out across the sea on a secret quest to set things right.",
          popularity: 32.704,
          poster_path: "/hg1959yuBkHb4BKbIvETQSfxGCT.jpg",
          release_date: "2009-09-03",
          title: "Tinker Bell and the Lost Treasure",
          video: false,
          vote_average: 6.8,
          vote_count: 705,
        },
        {
          adult: false,
          backdrop_path: "/fYr0fqT9NImOuaN1QgnDHgGh4Ci.jpg",
          genre_ids: [16, 10751, 12, 878],
          id: 10865,
          original_language: "en",
          original_title: "Atlantis: The Lost Empire",
          overview:
            "The world's most highly qualified crew of archaeologists and explorers is led by historian Milo Thatch as they board the incredible 1,000-foot submarine Ulysses and head deep into the mysteries of the sea. The underwater expedition takes an unexpected turn when the team's mission must switch from exploring Atlantis to protecting it.",
          popularity: 29.342,
          poster_path: "/8fUEFPUTF7kBMuKPiSQHxPvd8EZ.jpg",
          release_date: "2001-06-02",
          title: "Atlantis: The Lost Empire",
          video: false,
          vote_average: 6.9,
          vote_count: 3556,
        },
        {
          adult: false,
          backdrop_path: "/5HKdFlSWI6U7CjyNAHH6xJHQZHX.jpg",
          genre_ids: [878, 12],
          id: 2157,
          original_language: "en",
          original_title: "Lost in Space",
          overview:
            "The prospects for continuing life on Earth in the year 2058 are grim. So the Robinsons are launched into space to colonize Alpha Prime, the only other inhabitable planet in the galaxy. But when a stowaway sabotages the mission, the Robinsons find themselves hurtling through uncharted space.",
          popularity: 15.837,
          poster_path: "/4miEpZmUOMqV8P0T6oq5HVBiVHw.jpg",
          release_date: "1998-04-03",
          title: "Lost in Space",
          video: false,
          vote_average: 5.3,
          vote_count: 871,
        },
        {
          adult: false,
          backdrop_path: "/mTYeUMSUom113bHTiyvg7ValozG.jpg",
          genre_ids: [27, 35],
          id: 1547,
          original_language: "en",
          original_title: "The Lost Boys",
          overview:
            "A mother and her two teenage sons move to a seemingly nice and quiet small coastal California town yet soon find out that it's overrun by bike gangs and vampires. A couple of teenage friends take it upon themselves to hunt down the vampires that they suspect of a few mysterious murders and restore peace and calm to their town.",
          popularity: 12.249,
          poster_path: "/nH1lvyQvfbL5GKScTtT6zkIvDEn.jpg",
          release_date: "1987-07-31",
          title: "The Lost Boys",
          video: false,
          vote_average: 7,
          vote_count: 1335,
        },
        {
          adult: false,
          backdrop_path: "/j1FMMJhWWK3im0XtnBAYm9IaEXD.jpg",
          genre_ids: [18, 10749],
          id: 17612,
          original_language: "en",
          original_title: "Lost and Delirious",
          overview:
            "LOST AND DELIRIOUS is the story of three adolescent girls' first love, their discovery of sexual passion, and their search for identities. Set in a posh, private boarding school surrounded by luxuriant, green forest, LOST AND DELIRIOUS moves swiftly from academic routine, homesickness, and girlish silliness to the darker region of lover's intrigue.",
          popularity: 12.919,
          poster_path: "/3Cu95A09arsfTsOJfygVwhJe5qc.jpg",
          release_date: "2001-01-21",
          title: "Lost and Delirious",
          video: false,
          vote_average: 6.9,
          vote_count: 380,
        },
        {
          adult: false,
          backdrop_path: "/5rKa5UKXnTdLsgY0mJbjAEQX3gB.jpg",
          genre_ids: [28, 12, 10751, 35],
          id: 9488,
          original_language: "en",
          original_title: "Spy Kids 2: The Island of Lost Dreams",
          overview:
            "Exploring the further adventures of Carmen and Juni Cortez, who have now joined the family spy business as Level 2 OSS agents. Their new mission is to save the world from a mad scientist living on a volcanic island populated by an imaginative menagerie of creatures. On this bizarre island, none of the Cortez's gadgets work and they must rely on their wits--and each other--to survive and save the day.",
          popularity: 58.958,
          poster_path: "/A6gkSQVkbUiSCq7C9kexlJF8GdI.jpg",
          release_date: "2002-08-07",
          title: "Spy Kids 2: The Island of Lost Dreams",
          video: false,
          vote_average: 5.6,
          vote_count: 1611,
        },
        {
          adult: false,
          backdrop_path: "/4EMd9DU86rbd9XCjOjLHp5Khtn8.jpg",
          genre_ids: [53, 10749],
          id: 255343,
          original_language: "en",
          original_title: "Escobar: Paradise Lost",
          overview:
            "For Pablo Escobar family is everything. When young surfer Nick falls for Escobar's niece, Maria, he finds his life on the line when he's pulled into the dangerous world of the family business.",
          popularity: 15.59,
          poster_path: "/4HngNLzCmUYCPB8FbxSZWN0eDKM.jpg",
          release_date: "2014-10-11",
          title: "Escobar: Paradise Lost",
          video: false,
          vote_average: 6.3,
          vote_count: 621,
        },
        {
          adult: false,
          backdrop_path: "/a85JeaXynR7ViVX6pTbuxHgH9pB.jpg",
          genre_ids: [28, 12, 18],
          id: 152747,
          original_language: "en",
          original_title: "All Is Lost",
          overview:
            "During a solo voyage in the Indian Ocean, a veteran mariner awakes to find his vessel taking on water after a collision with a stray shipping container. With his radio and navigation equipment disabled, he sails unknowingly into a violent storm and barely escapes with his life. With any luck, the ocean currents may carry him into a shipping lane -- but, with supplies dwindling and the sharks circling, the sailor is forced to face his own mortality.",
          popularity: 11.098,
          poster_path: "/9cVA4oX2xHgiglv6hemxwAaofsq.jpg",
          release_date: "2013-08-23",
          title: "All Is Lost",
          video: false,
          vote_average: 6.6,
          vote_count: 1224,
        },
        {
          adult: false,
          backdrop_path: "/rLSfzNLViUMzjcFp0iWeZMY52pv.jpg",
          genre_ids: [14, 53, 18],
          id: 167810,
          original_language: "en",
          original_title: "Lost River",
          overview:
            "A single mother is swept into a dark underworld, while her teenage son discovers a road that leads him to a secret underwater town.",
          popularity: 8.422,
          poster_path: "/paG0O9cVcoQcXpNG8Nf0AnL7VWE.jpg",
          release_date: "2015-04-08",
          title: "Lost River",
          video: false,
          vote_average: 5.9,
          vote_count: 464,
        },
        {
          adult: false,
          backdrop_path: "/8UsLpipCADJWP4NVvfRKlR40jR6.jpg",
          genre_ids: [28],
          id: 498739,
          original_language: "en",
          original_title: "Spider-Man: Lost Cause",
          overview:
            "Peter Parker a lone child discovers that his parents were in a horrifying plot to make mankind change. getting bitten by his fathers invention he develops super powers to tries to find answers to his whole life, try and juggle a relationship with his girlfriend and try and find the murderer of his uncle. (Fan Made Film)",
          popularity: 10.543,
          poster_path: "/hzMvtGHYJwdhTBG1TSZrU3j96ka.jpg",
          release_date: "2014-09-26",
          title: "Spider-Man: Lost Cause",
          video: false,
          vote_average: 0,
          vote_count: 0,
        },
        {
          adult: false,
          backdrop_path: "/sKEqdZ3hhTrWbyWTJstRqVB2PMN.jpg",
          genre_ids: [28, 12, 36],
          id: 526746,
          original_language: "en",
          original_title: "The Lost Viking",
          overview:
            "A young Viking called Vitharr arrives in Britain with dreams of conquest and adventure, but when his family and clan are ambushed and killed, he must survive alone in this strange,dangerous new land as he searches for his Uncle's settlement.",
          popularity: 10.459,
          poster_path: "/9gFHSGKV5EZxJe6d6qsROpAiBgQ.jpg",
          release_date: "2018-05-28",
          title: "The Lost Viking",
          video: false,
          vote_average: 6.3,
          vote_count: 139,
        },
        {
          adult: false,
          backdrop_path: "/mwXmcrvjOJwzsJSuNEupjisXUt6.jpg",
          genre_ids: [18],
          id: 479259,
          original_language: "en",
          original_title: "Lost Girls & Love Hotels",
          overview:
            "Searching for escape in Tokyo's back alleys, a haunted English teacher explores love and lust with a dashing Yakuza, as their tumultuous affair takes her on a journey through the city's dive bars and three-hour love hotels.",
          popularity: 14.055,
          poster_path: "/vQgXwuJrlpzGDI8169tRQRy71Nv.jpg",
          release_date: "2020-09-18",
          title: "Lost Girls & Love Hotels",
          video: false,
          vote_average: 5.4,
          vote_count: 89,
        },
      ],
    };
  },
  filters: {
    releaseDate(date) {
      return new Date(date).getFullYear();
    },
  },
  methods: {
    customLabel({ title }) {
      return `${title}`;
    },
  },
};
</script>
<style lang="scss">
.color-primary {
  color: #354ef7;
}
.title {
  align-items: baseline;
  display: flex;
  justify-items: center;
  .container-multiselect {
    border-bottom: 3px solid #354ef7;
    margin: 0px 10px;
  }
}

.multiselect__select {
  display: none;
}

.multiselect__tags {
  border: none;
  align-items: center;
  display: flex;
  padding: 8px 0px;
  font-size: 1.5em;
}

.option__image {
  width: 40px;
}

.multiselect__single {
  margin-bottom: 0px;
  font-size: 1em;
}

.container-option {
  display: flex;
}

.option__desc {
  flex-direction: column;
  flex-wrap: wrap;
  display: flex;
  margin: 0px 10px;
}

.option__title,
.option__small {
  margin-bottom: 5px;
  font-weight: 400;
}

.img-icon {
  width: 20px;
  height: 20px;
}

.controls {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
}

.align-flex-start {
  display: flex;
  align-items: flex-start;
}
</style>
