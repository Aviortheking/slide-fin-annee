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
Soutenance de fin d'étude
ne pas dire campus academy au début


TODO:
moins bouger les mains

demande de l'entreprise

meileurs vocabulaire

bouteille d'eau

donner des exemples pour les partis du code


savoir faire evolué avel le logiciel
-->

---
layout: content-2
---

# Sommaire

<v-click>

- Introduction
	- Parcours professionnel
	- Présentation de l'entreprise Aptatio
	- Contexte du projet

</v-click>

<v-click>

- Conception
	- Gestion de projet
	- Interface de l'application
	- Spécifications

</v-click>

<v-click>

- Réalisation
	- Développement du Front
	- Développement du Back
	- Tests Unitaire et Déploiement

</v-click>

<v-click>

- Conclusion

</v-click>

<!--
introduire soutenance avec mon parcours, pres aptatio, et le projet
-->

---
layout: section-1
---

# 1. Introduction

___

Parcours professionnel  
Présentation de l'entreprise Aptatio  
Contexte du projet: AptaHome

<!--
commencer par l'intro
-->

---
layout: image-fullscreen-2
---

<div class="py-16 pl-64">

# Parcours professionnel

</div>

<!--
- Passionnée d'informatique depuis longtemps
- vacances sur le fonctionnement d'un ordinateur
- Études SEN
- rejoinds Campus Academy 3 ans
- Aptatio en stage puis alternance
- tous sa permis projets Typescript/languages web, c++ Arduino, app mobile Kotlin
-->

---
layout: image-fullscreen-1
---

<div class="py-16">

# L'entreprise

</div>

<!--
Bureau d'étude
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
- entreprise Experte depuis plus de 8 ans dans le domaine du design produit, prototypage, développement logiciel
- permet accomapgnement client complet, prototypage => industrialisation passant logiciel/electronique.
- nouveau locaux
- dire ce que j'ai fait dans l'entreprise
Parler de l'exemple
-->

---
layout: section-1
image: ../logo-aptahome.png
---

# Le Projet

<div class="flex justify-center flex-grow-0">
<img src="/logo-aptahome.png" style="width: 40%; " />
</div>

<div v-click class="py-1 text-xl">

Contexte

</div>

<div v-click class="text-xl">

Objectifs et Enjeux

</div>


<div v-click class="py-1 text-xl">

Contraintes

</div>

<!--
Projet AptaHome
This is a software that allow to easily manage administrative documents for the company via multiple solutions, like managing documents templates, automaticly sending exported documents to the Samba server and of course manage multiple types of documents.

Contexte: POURQUOI
- débuté début 2020
- automatisation des documents pro
- reduction temps création documents

Objectifs: qu'est-ce que sa fait

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

<div class="flex justify-center flex-grow-0 py-8">
	<img src="https://i.pinimg.com/736x/ce/50/13/ce50136d82119dbab571192a828556cd.jpg" style="width: 50%" />
</div>

<!--
- Méthode Agile
	- rdv tout les vendredi
	- résumé des changement éfféctué pendant la semaine
	- tests des changements et de la solution en global
-->

---
layout: section-2
---

# Gestion du travail


<div class="flex justify-center flex-grow-0 py-4">
	<img src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Flogos-download.com%2Fwp-content%2Fuploads%2F2016%2F09%2FGitHub_logo.png&f=1&nofb=1" style="width: 20%" />
</div>

<div v-click class="flex justify-center flex-grow-0 py-4">
	<img src="/method.png" />
</div>

<div v-after class="flex justify-center flex-grow-0 py-4">
	<img src="/labels.png" style="width: 50%" />
</div>

<!--

Code Stocké sur Github

KANBAN

- Kanban
	- todo automatique
    - in prgs taches active
    - done faite
    
- Code stocké sur Github
-->

---
layout: section-2
name: Environments du Logiciel
---

# Environments du Logiciel


<div class="flex justify-center flex-grow-0 py-4">
	<img src="/monitor.svg" style="width: 20%" />
</div>

<div v-click class="flex justify-center flex-grow-0 py-4">
	<img src="https://caprover.com/img/logo.png" style="width: 20%" />
</div>


<!--

KANBAN

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
Diagramme de cas d'utilisation
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
layout: image-reverse
image: ../graphique-index.png
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
layout: image-reverse
image: ../proto-graphique.png
name: Prototypage Graphique
---

<div class="text-6xl">
Prototypage Graphique
</div>

<!--
- Prototypage Graphique

Tester l'UI/UX du logiciel
tester l'usage
-->

---
layout: image-reverse
image: ../assets.png
name: Assets Graphique
---

<div class="text-6xl">
Assets<br />Graphique
</div>

<!--
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
	.from<Props>('serverSideProps')
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
layout: image-reverse
image: "tpl-2.png"
name: Développement du Back - Gestion de Templates
---

<div class="text-5xl">
Développement<br />du Back
</div>

<div class="py-4 text-3xl">
Gestion de templates
</div>

<div class="py-4">
	<img src="/tpl-1.png" style="width: 20%" />
</div>

<!--
TODO: show some XML

Structure ODT + d'un template
-->

---
layout: content-1
name: Développement du Back - Gestion de Templates - Compilation de templates
---

<div class="text-5xl">
Développement du Back
</div>

<div class="py-4 text-3xl">
Compilation de templates
</div>

```ts {all|2-3|5-6|8-13|15-17|all}
public async compileText(content: string): Promise<string> {
	// Load XML Content
	const xml = await XML.parseAsync(content)

	// Process Document
	this.scanTag(xml)

	// Register Handlerbars helpers
	Handlebars.registerHelper('inc', (item) => item + 1)
	Handlebars.registerHelper('equal', function equalHelper(a, b, opts: HelperOptions) {
		return a == b ? opts.fn(this) : opts.inverse(this)
	})
	Handlebars.registerHelper('isNotZero', (item) => item !== 0)

	// Run Handlebars in the file
	const tpl = Handlebars.compile(built)
	return tpl(this.input)
}
```

<!--
Explication compilation Template
-->

---
layout: content-2
name: Développement du Back - Gestion de Templates - Problèmes Handlebars et corrections faites
---

<div class="text-5xl">
Développement du Back
</div>

<div class="py-4 text-3xl">
Problèmes Handlebars et corrections faites
</div>

```xml
<text:p text:style-name="P20">
  <text:span text:style-name="T32">Objet</text:span>
  <text:span text:style-name="T33">: </text:span>
  <text:span text:style-name="T14">{{obj</text:span>
  <text:span text:style-name="T15">ec</text:span>
  <text:span text:style-name="T16">t}}</text:span>
</text:p>
```

<v-click>


```xml
<text:p text:style-name="P20">
  <text:span text:style-name="T32">Objet</text:span>
  <text:span text:style-name="T33">: </text:span>
  <text:span text:style-name="T16">{{objectt}}</text:span>
</text:p>
```

</v-click>

<!--
- Handlebars cant compile [] items so they have to be precompiled to a handlebar compatible ones
- We have to fix LibreOffice misschiefs or handlebars will not be able to compile it
-->

---
layout: content-2
name: Développement du Back - Gestion de Templates - Problèmes Handlebars et corrections faites
---

<div class="text-5xl">
Développement du Back
</div>

<div class="py-4 text-3xl">
Problèmes Handlebars et corrections faites
</div>

```xml
<table:table table:name="Table1" table:style-name="Table1">
	<table:table-column table:style-name="Table1.A" />
	<table:table-column table:style-name="Table1.B" />
	<table:table-header-rows>
		<table:table-row table:style-name="Table1.1">
			<table:table-cell table:style-name="Table1.A1" office:value-type="string">
				<text:p text:style-name="P17">BL</text:p>
			</table:table-cell>
		</table:table-row>
	</table:table-header-rows>
	<table:table-row table:style-name="Table1.2">
		<table:table-cell table:style-name="Table1.A2" office:value-type="string">
			<text:p text:style-name="P26">[table item=«designations»]{{../id}}{{@index}}</text:p>
		</table:table-cell>
	</table:table-row>
</table:table>
```

<!--
- Handlebars cant compile [] items so they have to be precompiled to a handlebar compatible ones
- We have to fix LibreOffice misschiefs or handlebars will not be able to compile it
-->

---
layout: content-2
name: Développement du Back - Gestion de Templates - Problèmes Handlebars et corrections faites
---

<div class="text-5xl">
Développement du Back
</div>

<div class="py-4 text-3xl">
Problèmes Handlebars et corrections faites
</div>

```xml
<table:table table:name="Table1" table:style-name="Table1">
	<table:table-column table:style-name="Table1.A" />
	<table:table-column table:style-name="Table1.B" />
	<table:table-header-rows>
		<table:table-row table:style-name="Table1.1">
			<table:table-cell table:style-name="Table1.A1" office:value-type="string">
				<text:p text:style-name="P17">BL</text:p>
			</table:table-cell>
		</table:table-row>
	</table:table-header-rows>
	{{#each designations}}
	<table:table-row table:style-name="Table1.2">
		<table:table-cell table:style-name="Table1.A2" office:value-type="string">
			<text:p text:style-name="P26">{{../id}}{{@index}}</text:p>
		</table:table-cell>
	</table:table-row>
	{{/each}}
</table:table>
```

<!--
- Handlebars cant compile [] items so they have to be precompiled to a handlebar compatible ones
- We have to fix LibreOffice misschiefs or handlebars will not be able to compile it
-->

---
layout: section-1
name: Développement du Back - Gestion de Templates - Exemple de document
---

<div class="text-5xl">
Développement du Back
</div>

<div class="py-4 text-3xl">
Exemple de document
</div>

<div class="flex direction-row justify-even">
	<div class="py-4 px-4">
		<img src="/bon-template.png"/>
	</div>
	<div class="py-4 px-4">
		<img src="/bon-filled.png"/>
	</div>
</div>

<!--
- Handlebars cant compile [] items so they have to be precompiled to a handlebar compatible ones
- We have to fix LibreOffice misschiefs or handlebars will not be able to compile it
-->

---
layout: content-2
name: Tests unitaires
---

# Tests unitaire

<div class="py-2">
	<img src="/unit-test-1.png" style="width: 60%" />
</div>

<div v-click class="mx-32 py-2">
	<img src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.freebiesupply.com%2Flogos%2Flarge%2F2x%2Fjest-logo-png-transparent.png&f=1&nofb=1" style="width: 25%" />
</div>

<!--
donner un exemple avec les tests de parsing et de stringify de XML
-->

---
layout: content-2
name: Tests unitaires - Example
---

# Tests unitaire

```ts {all|3-10|12-19|all}
const XML = require('../../src/libs/XML').default

test('Parsing a full document should work', async () => {
	const res = await XML.parseAsync('<test at="p">p1<child>c1</child>p2</test>')
	expect(res).toEqual({
		name: 'test',
		attrs: [{key: 'at', value: 'p'}],
		childs: ['p1', {name: 'child', childs: ['c1']}, 'p2']
	})
})

test('Stringify Should escape expected characters in values', async () => {
	const res = await XML.stringifyAsync({
		name: 'test',
		attrs: [{key: 'test', value: '&"\'<>'}],
		childs: ['&"\'<>']
	})
	expect(res).toMatchSnapshot()
})
```

```ts
exports[`Stringify Should escape expected characters in values 1`] =
	`"<test test=\\"&amp;&quot;&apos;&lt;&gt;\\">&amp;&quot;&apos;&lt;&gt;</test>"`;
```

<!--
donner un exemple avec les tests de parsing et de stringify de XML
-->

---
layout: content-2
name: Déploiement
---

<div class="text-5xl">
Déploiement du logiciel
</div>

```dockerfile {all|1-11|12-24|all}
FROM node:alpine as BUILD_IMAGE

WORKDIR /app

ADD package.json package-lock.json ./

RUN npm i

ADD . .

RUN npm run build && npm prune --production

FROM node:alpine

WORKDIR /app

COPY --from=BUILD_IMAGE /app/package.json ./package.json
COPY --from=BUILD_IMAGE /app/node_modules ./node_modules
COPY --from=BUILD_IMAGE /app/.next ./.next
COPY --from=BUILD_IMAGE /app/public ./public

EXPOSE 3000

CMD ["npm", "run", "start"]
```

<!--
Montrer le Dockerfile

Montrer déplloiement sur Caprover
-->

---
layout: image
image: /deploy-1.png
name: Déploiement - Caprover
---

<div class="text-5xl">
Déploiement du logiciel
</div>

<div class="flex justify-center flex-grow-0 py-16">
	<img src="https://caprover.com/img/logo.png" style="width: 40%" />
</div>

---
layout: section-1
---

# Conclusion

<!--

## Projet

- évolué avec ce projet
- pas mal de difficultés (templates) et j'en ai encore
- mais le voir aujourdhui utilise par mes collègues et patron
- sentiment de fièreté


## Global

- années dans le domaine du dev
- forger une passion inconditionnel
- beaucoup apris au cours des dernières années
- en companige de Campus Academy
- de mon entreprise
-->

---
layout: end
---

# Merci
## de votre attention !
