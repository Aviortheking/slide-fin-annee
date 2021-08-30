---
theme: zhozhoba
layout: cover
highlighter: prism
lineNumbers: false
company: Campus Academy
---

# Concepteur Développeur d'Application

---
layout: content-1
---

# Sommaire

- Introduction
	- Parcours professionnel
	- L'entreprise
	- Le Projet
- Conception
	- Méthode de travail
	- Conception Graphique
	- Spécifications
- Réalisation
	- Développement du Front
	- Développement du Back
	- Tests Unitaire et Déploiement
- Conclusion


---
layout: section-1
---

# 1. Introduction

---
layout: section-2
---

# Parcours professionnel

<!--
Avant d’arriver dans mon alternance  est  à  Campus Academy, j’ai effectué  des 
études de Système électronique et numérique. 
J’ai toujours été passionnée par l’informatique depuis ma plus tendre enfance le 
fait de toujours avoir à découvrir des nouvelles technologies et la vitesse d’avancement 
de l’informatique on en fait un domaine que j’ai apprécié. 
Après avoir tester pendant des vacances d’été j’ai souhaité rejoindre l’IMIE qui est 
devenu Campus Academy afin de me professionnaliser dans le domaine du 
développement logiciel. 
J’ai rejoint l’entreprise Aptatio en alternance car je les connaissais déjà par des 
stages précédent le centre de formation afin de pouvoir beaucoup plus évoluer par moi-
même. 
Au cours de mes 2 ans en alternance, j’ai pu participer a beaucoup de projets chez 
Aptatio, en passant par le développement en C++ de modules Arduino au logiciels Web 
complet, comme l’AptaHome que je vais présenter dans la suite de ce document. 
Après  mon  alternance,  et  par  déception  de  mes  dernières  années  au  centre  de 
formation j’ai décidé avec mes supérieurs de rejoindre à temps plein l’entreprise Aptatio.
-->

---
layout: section-2
---

# L'Entreprise

<div class="flex justify-center flex-grow-0 py-8">
<img src="https://www.aptatio.com/wp-content/uploads/2019/06/LOGO_APTATIO_I.png" style="width: 80%; " />
</div>

<!--
La Société Aptatio est un expert dans les domaines du Design produit, Prototypage 
et Développement Logiciel, avec plus de 8 ans d’existence, elle accompagne ses clients 
dans  la  création  du  design d’objets connectés, du prototypage fonctionnel jusqu’à son 
industrialisation en passant par son logiciel et électronique. 
 
Elle  est  aussi  centre  de  formation  sur  toute  la  chaine  numérique  3D,  elle  forme  des   
professionnels   à   la   modélisation   3D   jusqu’à   la   fabrication   objet   par impression 
3D. 
Elle  a  créé  plus  d’un  millier  de  différents  objets,  logiciels  et  designs  pour  ses 
différents clients qui inclus L’Oréal ou encore Orange.
-->

---
layout: section-2
---

# Le Projet

<div v-after class="text-4xl">

Contexte

</div>
  
<div v-click class="py-8 text-4xl">

Objectifs et Enjeux

</div>


<div v-click class="text-4xl">

Contraintes

</div>

<!--
Contexte

- débuté début 2020
- automatisation
- automatisation des documents

Objectifs

- centralisation documents entreprise
- template de document


Contraintes fonctionnel

- Simplicité d'utilisation
- Liaison avec Dolibarr

Contraintes Technique

- Language simple
- Conteneur

Contraintes de qualité

- primordial
- maintenable
- facilité d'utilisation

Délais

- Premier proto 2018
- début 2021
- fin mi-2021
-->

---
layout: section-1
---

# 2. Conception

---
layout: section-2
---

# Méthode de travail

<v-click>
	<div class="flex justify-center flex-grow-0 py-8">
		<img src="/method.png" />
	</div>
</v-click>

<!--
- Méthode Agile
	- rdv hebdomadaire
    - test des elements du système

*click*

- Kanban
	- todo automatique
    - in prgs taches active
    - done faite
-->

---
layout: image
image: ../uml-use.png
name: spécification fonctionnelle
---

<div class="text-6xl">
Spécifications
</div>

<div class="py-4 text-3xl">
Spécification&nbsp;Fonctionnelle
</div>

<!--
Fonctionnelle

- Page 14 du doc un cas d'utilisation UML

- Authentification: Sécurité
- Édition de documents: Édition simple de documents

- Filtrage: recherche de documents
- Export: Export de documents/vues
-->

---
layout: image
image: ../archi-app.png
name: spécification Technique
---

<div class="text-6xl">
Spécifications
</div>

<div class="py-4 text-3xl">
Spécification Technique
</div>

<!--
Technique

- Architecture Applicattif
	- partie client web
    	- vues utilisateur
    - partie serveur
        - auth, models, controllers, REST API

Technologies utilisés
- NextJS
	- MVC
    - Typescript
    - Front: React
    - API REST
    - MariaDB
- caprover
	- PaaS (Platform as a Service)
-->

---
layout: image
image: ../front.PNG
name: Conception Graphique
---

<div class="text-6xl">
Conception Graphique
</div>

<!--
- Maquettage sur Figma

- Prototypage Graphique

- Popup customisable
-->

---
layout: section-1
---

# 3. Réalisation

---
layout: section-2
name: Développement du Front
---

<div class="text-5xl">
	Développement du Front
</div>

```ts {1-5|7-19|all}
interface Props {
	offers: Array<OfferModel>
	contacts: Array<ContactModel>
	tiers: Array<TierModel>
}

interface Filters {
	year?: string
	month?: string
	status?: string
	tier?: string
	name?: string
}

interface States extends Filters {
	sort: string
	filteredOffers?: Array<OfferModel>
	offset: number
}
```

---
layout: section-2
name: Développement du Front 2
---

<div class="text-5xl">
	Développement du Front
</div>

```ts {all|9-12}
export default class OffersRoute extends React.Component<Props, States> {

	public render = () => (
		<Row direction="column">
			<Col>
				...
			</Col>
			<Col>
				<Button
					disabled={this.state.offset === 0}
					onClick={() => this.setState({offset: this.state.offset - 1})}
				>Page précédente</Button>
			</Col>
		</Row>
	)

}
```


---
layout: section-2
name: Développement du Back - DB 1
---

<div class="text-5xl">
Développement du Back
</div>

<div class="py-4 text-3xl">
Modèles de donnée
</div>

```ts {1-6|7|8-14|15-16|all}
export interface BonModel {
  id: number
  customId?: string
  designations?: Array<string>
  Offer?: OfferModel
}
class Bon extends Model<Omit<BonModel, 'Users'>> implements BonModel {}
Bon.init({
  customId: DataTypes.STRING,
  designations: jsonField('designations'),
}, {
  sequelize,
  tableName: 'bon'
})
Offer.hasOne(Bon)
Bon.belongsTo(Offer)
export default Bon
```

<!--
```sql
CREATE TABLE `bon` (
  `id` int PRIMARY KEY AUTO_INCREMENT,
  `customId` varchar(255),
  `designations` text,
  `offer_id` int
);

CREATE TABLE `offer` (
  `id` int PRIMARY KEY AUTO_INCREMENT
);

ALTER TABLE `users` ADD FOREIGN KEY (`offer_id`) REFERENCES `offer` (`id`);
```
-->

---
layout: section-2
name: Développement du Back - DB 2
---

<div class="text-5xl">
Développement du Back
</div>

<div class="py-4 text-3xl">
Modèles de donnée
</div>

```sql
CREATE TABLE `bon` (
  `id` int PRIMARY KEY AUTO_INCREMENT,
  `customId` varchar(255),
  `designations` text
);

ALTER TABLE `users` ADD FOREIGN KEY (`offer_id`) REFERENCES `offer` (`id`);
```

<!--
```sql
SELECT * FROM bon INNER JOIN offer.id = bon.offer_id
```
-->
