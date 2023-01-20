<template>
  <h2>Resume</h2>
  <div class="row">
    <div class="col">
      <p class="text-body1">
        Je suis actuellement ingénieur de recherche en courtage des données à
        l’Institut Français de Bioinformatique. L’objectif de ma mission est
        d’assurer l’orchestration des flux de données tout au long de la vie des
        projets de recherche, depuis leur production jusqu’à leur valorisation
        dans les banques de données internationales, en passant par les chaînes
        de traitement et d’analyse, et en établissant des liens avec les
        informations contenues dans le Plan de Gestion de Données (PGD). <br />
        <br />
        En parallèle de cette activité, je suis impliqué dans la formation
        continue en bioinformatique proposé par l’Institut Français de
        Bioinformatique .
      </p>
    </div>
    <div class="col"></div>
  </div>
  <div class="row">
    <div class="col">
      <h3>Recherche</h3>
      <p><b>Mots clés</b></p>
      <div class="q-gutter-xs">
        <q-chip
          square
          color="primary"
          text-color="white"
          v-for="(c, index) in recherche_chips"
          :key="index"
        >
          {{ c }}
        </q-chip>
      </div>

      <p><b>Productions scientifiques</b></p>
      <ul>
        <li>9 articles scientifiques (dont 4 en premier auteur)</li>
        <li>3 communications orales et 9 affichées (2 posters primés)</li>
        <li>
          5 applications WEB (bPeaks App, PIXEL Web App, Pixel2, START-R, MONet)
        </li>
        <li>
          Outil de visualisation de réseaux de gènes coexprimés (iHKG viewer)
        </li>
      </ul>

      <p><b>Productions scientifiques</b></p>
      <ul>
        <li>Encadrement Stage d’une étudiante en L2 Biologie (2018)</li>
        <li>Encadrement Stage d’une étudiante en L3 Biologie (2022)</li>
        <li>Encadrement Stage d’un étudiant en M2 Bioinformatique (2023)</li>
      </ul>
      <p><b>Sur les réseaux de recherche</b></p>
      <p>ORCID - ResearchGate - scienceOPEN</p>
    </div>
    <div class="col">
      <h3>Enseignements</h3>
      <p><b>Mots clés</b></p>
      <div class="q-gutter-xs">
        <q-chip
          square
          color="primary"
          text-color="white"
          v-for="(c, index) in teaching_chips"
          :key="index"
        >
          {{ c }}
        </q-chip>
      </div>

      <p><b>Formation initiale</b></p>
      <ul>
        <li>
          IUT Informatique - Orsay : Introduction à l'Algorithmique et à la
          Programmation C++ ; Conception de documents et interfaces numériques ;
          Introduction de base à la Programmation Orientée Objet en Java (Total
          : 64h/an)
        </li>
        <li>
          ENS Cachan : UE Initiation à la recherche : outils scientifiques
          (Licence 3) - Création du contenu pédagogique
        </li>
      </ul>

      <p><b>Formations professionnelles</b></p>
      <ul>
        <li>
          Formation à la reproductibilité “FAIR_Bioinfo - Formation et
          protocoles clé en main pour une biologie computationnelle
          reproductible” - GitHub
        </li>
        <li>
          Création du contenu pédagogique Formateur à l’école de bioinformatique
          AVIESAN-IFB de Roscoff “Initiation au traitement des données de
          génomique obtenues par séquençage à haut débit” - Atelier RNAseq -
          Site web
        </li>
        <li>
          Formateur au Diplôme universitaire "Création, analyse et valorisation
          de données omiques" - Site web
        </li>
      </ul>
    </div>
  </div>
  <h2>Compétences</h2>

  <Skill progress=0.9 />

  <h2>Formation</h2>
  <p>
    Mon parcours scientifique a débuté en tant que technicien dans les
    laboratoires de l’Assistance Publique des Hôpitaux de Paris (période 2011 –
    2014). J’ai observé l’arrivée des premiers séquenceurs à très haut débit
    (technologie Illumina). Pour mes collègues, une problématique majeure de
    l’utilisation de ces nouveaux appareils était la gestion, l’organisation et
    le traitement de la grande quantité de données générées (plusieurs Giga
    octets pour une seule analyse). Dans ce contexte, j’ai décidé de reprendre
    mes études. Souhaitant acquérir les compétences nécessaires à l’analyse de
    ces nouvelles informations biologiques, j’ai ainsi réalisé une Licence 3
    puis un Master en Bioinformatique. En septembre 2020, j'ai obtenu mon
    doctorat en bioinformatique et analyse de données à l’Université
    Paris-Saclay.
  </p>

  <q-timeline color="secondary">
    <q-timeline-entry
      title="Doctorat - Paris Saclay"
      subtitle="2020"
      body="École doctorale Structure et Dynamique des Systèmes Vivants - Paris Sud - Paris Saclay"
    />
    <q-timeline-entry
      title="Doctorant à l’Université Paris Sud - Paris Saclay"
      subtitle="2017-2020"
      body="École doctorale Structure et Dynamique des Systèmes Vivants - Paris Sud - Paris Saclay"
    />
    <q-timeline-entry
      title="..."
      subtitle="..."
      body="..."
    />
  </q-timeline>
  
</template>

<script>
export default {
  data: () => ({
    recherche_chips: [
      "Biologie computationnelle",
      "Bioinformatique",
      "Biostatistiques",
      "Data science",
      "Data brokering",
      "Omics",
      "Programmation et développement",
    ],
    teaching_chips: [
      "Programmation",
      "Web design",
      "Reproductibilité",
      "Bioinformatique",
      "Analyse de données omiques",
    ],
  }),
};
</script>

<style lang="scss" scoped>
h2,
h3,
h4 {
  color: $myBlue;
}

h2::after {
  content: "";
  display: block;
  width: 300px;
  height: 3px;
  background: $mylightBlue !important;
  margin-top: 3px;
  box-sizing: border-box;
}
.bg-myBlue {
  background: $myBlue !important;
}

.myBlue {
  color: $myBlue !important;
}
</style>