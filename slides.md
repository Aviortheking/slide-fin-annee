---
theme: zhozhoba
layout: cover
highlighter: prism
lineNumbers: false
company: Campus Academy
title: Concepteur Développeur d'Application
---

# Concepteur Développeur d'Application
## Florian BOUILLON - 2021

<!--
TODO: trouver une bonne intro
-->

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

___

Parcours professionnel  
Aptatio  
Le projet: AptaHome

<!--
commencer par l'intro
-->

---
layout: section-2
---

# Parcours professionnel

<!--
- Passionnée d'informatique depuis longtemps
- vacances d'été j'ai adoré
- Études SEN => SN
- rejoinds l'IMIE -> Campus Academy
- Aptatio en stage puis alternance
- au cours des dernières - projets Typescript/languages web, c++ Arduino, app mobile Kotlin
-->

---
layout: section-2
---

# L'Entreprise

<div class="flex justify-center flex-grow-0">
<img src="https://www.aptatio.com/wp-content/uploads/2015/06/00-connecth-inh-.jpg" style="width: 70%; " />
</div>

<div class="flex justify-center flex-grow-0 py-8">
<img src="https://www.aptatio.com/wp-content/uploads/2019/06/LOGO_APTATIO_I.png" style="width: 50%; " />
</div>

<!--
- Aptatio
- entreprise Experte dans le domaine du design produit, prototypage, développement logiciel
- 8 ans d'exp
- domaines electronique et logiciel
- accomapgnement client, prototypage => industrialisation passant logiciel/electronique.
-->

---
layout: image
image: ../logo-aptahome.png
---

# Le Projet

<div v-after class="text-4xl">

L'aptaHome

</div>

<div v-click class="py-8 text-4xl">

Contexte

</div>

<div v-click class="text-4xl">

Objectifs et Enjeux

</div>


<div v-click class="py-8 text-4xl">

Contraintes

</div>

<!--
Projet AptaHome

Contexte
POURQUOI
- débuté début 2020
- automatisation des documents pro
- reduction temps création documents

Objectifs

- centralisation documents entreprise
- template de document
integrer au workflow
faire evoluier et ouvrir


Contraintes
difficulte'resumesr
- fonctionnel
	- Simplicité d'utilisation
	- Liaison avec Dolibarr
- Qualité
	- facilité d'utilisation
	- // cotés soft
	- maintenable
- Technique
	- Language simple
	- Conteneur

- Délais
	- Premier proto 2018
	- début 2021
	- fin mi-2021
-->

---
layout: section-1
---

# 2. Conception

______

Méthode de travail  
Spécifications Fonctionnel et Technique  
Conception Graphique

<!--
- intro conception AptaHome
-->

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

afficher KANBAN

- Kanban
	- todo automatique
    - in prgs taches active
    - done faite
    
- Code stocké sur Github
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
image: ../uml-seq.png
name: spécification Technique 2
---

<div class="text-6xl">
Spécifications
</div>

<div class="py-4 text-3xl">
Spécification Technique
</div>

<!--
Exemple de séquences faite pour la connexion

- montrer ce que NextJS dirige
- Montrer ce que Sequelize Dirige

- Montrer la sécurité
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
-->

---
layout: section-1
---

# 3. Réalisation

______

Développement du Front  
Développement du Back  
Tests Unitaire et Déploiement
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

<!--
TODO: Before this swho file structure
-->

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
name: Développement du Back - Controllers
---

<div class="text-5xl">
Développement du Back
</div>

<div class="py-4 text-3xl">
Controller
</div>

```ts {all|1-2,12|3|4-10|all}
export const getServerSideProps: GetServerSideProps<Props> = router
	.from<Prop>('serverSideProps')
	.get(async (ctx) => {
		const offers = await Offer.findAll()
		...
		return {
			props: {
				offers: offers
			}
		}
	})
.build()

```

<!--
Moins être un gogole loool
-->

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
- interface déclaration de colunnes de la table
	- noter que Offer est une jointure avec la table des offres
- class création du lien entre Sequelize et notre déclaration
- initialiser la table in db
- jointures faites ici

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

<v-click-hide>

```sql
CREATE TABLE `bon` (
  `id` int PRIMARY KEY AUTO_INCREMENT,
  `customId` varchar(255),
  `designations` text,
  PRIMARY KEY (`id`)
);

ALTER TABLE `bon` ADD FOREIGN KEY (`offer_id`) REFERENCES `offer` (`id`);
```
              
</v-click-hide>

<v-click>
  
```ts
await Bon.findById(21)
```

```sql
SELECT * FROM bon INNER JOIN offer.id = bon.offer_id WHERE bon.id = 21;
```

</v-click>

<!--
```sql
SELECT * FROM bon INNER JOIN offer.id = bon.offer_id
```
-->

---
layout: image
image: ../api-folders.PNG
name: Développement du Back - API 1
---

<div class="text-5xl">
Développement du Back
</div>

<div class="py-4 text-3xl">
API - Global
</div>

<v-click>

```ts {all|1,16|2,5|3,14|6-14|1-4}
export default router.from('api')
	.get(async (req, res) => {
		res.status(200).json(await Bon.findAll())
	})
	.post(async (req, res) => {
		const bon = Bon.build(
			req.body,
			{ include: [Offer] }
		)
		if (req.query.from) {
			bon.OfferId = parseInt(req.query.from, 10)
		}
		await bon.save()
		res.status(200).json({ id: bon.id, ok: true })
	})
	.build()
```

</v-click>

<!--
- Maquettage sur Figma

- Prototypage Graphique

- Popup customisable
-->

---
layout: image
image: ../api-folders.PNG
name: Développement du Back - API - Middleware
---

<div class="text-5xl">
Développement du Back
</div>

<div class="py-4 text-3xl">
API - Middleware
</div>

```ts {all|3|5-15|all}
const router = new Router<{token: string}>().use(
	(req) => {
		req.token = new Session(req).getSession()?.token

		if (
			!req.token &&
			!req.url?.startsWith('/login') &&
			!req.url?.startsWith('/_')
		) {
			return {
				redirect: {
					statusCode: 301,
					destination: `/login?redirect=${req.url}`
				}
			}
		}
	}
)
```

<!--
- Maquettage sur Figma

- Prototypage Graphique

- Popup customisable
-->

---
layout: end
---

# Merci
## de votre attention !
