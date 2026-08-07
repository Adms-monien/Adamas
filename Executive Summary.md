# Adamas

## Let's build the web4:

Infrastructure for food sovereignty, the real economy, autonomous coordination, and decentralized networks.


.


## Executive Summary

### The Problem

2.69 billion people — 32.7% of humanity — cannot afford a healthy diet. 645 million faced hunger in 2025.

The cost of eating well rose 46% in eight years: from $2.94 per person per day in 2017 to $4.28 in 2025. — 
State of Food Security and Nutrition in the World, 2026 edition. The figure continues to rise.

A figure that reveals the distortion: the international extreme poverty line is set at $3 per day, while 
eating healthily costs $4.28. Those just above the poverty line cannot afford to eat well.
The Paradox

The world grows 5,935 kilocalories per person per day of directly edible food. Only 2,531 reach people's mouths.
| Stage | Value |
|-------|-------|
| Harvest and soil | −338 kcal |
| Post-harvest | −332 kcal |
| International trade | −73 kcal |
| Biofuels | −808 kcal |
| Seed | −126 kcal |
| Fed to animals | −1,738 kcal |
| Returned as meat, dairy and fish | +594 kcal |
| Processing, distribution and waste | −586 kcal |
| Effectively eaten | 2,531 kcal |
| Average requirement | 2,353 kcal |
| Real surplus | 178 kcal — 8% |
Source: Berners-Lee, M., Kennelly, C., Watson, R., & Hewitt, C. N. (2018). Current global food production is 
sufficient to meet human nutritional needs in 2050 provided there is radical societal adaptation. Elementa: 
Science of the Anthropocene, https://doi.org/10.1525/elementa.310

The global food system produces just enough. And it produces just enough because it diverts nearly 
half of what is edible to uses that destroy nutritional value.

Grain-fed livestock is the largest diversion: it consumes the equivalent of 5,550 kilocalories per 
person per day and returns 594. A conversion rate of 12%.

In protein, the effect is worse: feeding edible crops to animals reduces available protein by 51 grams 
per person per day — 116% of what all of humanity needs.

The cost is not only human: livestock occupies 77% of agricultural land, provides only 18% of calories, 
and generates 14.5% of global emissions. Feeding without destroying the planet requires better coordination of
what already exists, not producing more. Adamas is that coordination infrastructure.

#### The Thesis

The problem is not production but destination, distribution, and price.

And a figure proves it: for every dollar spent on food, 11.8 cents reach the producer. After deducting 
their expenses, they keep between 2 and 3 cents. — USDA Economic Research Service, Food Dollar series, 2024.

The remaining 88.2 cents are processing, packaging, long-distance transport, wholesale intermediation, 
and retail margin — much of which a local circuit does not need.

### The Solution

Adamas is a coordination platform that enables communities to self-manage their economy and governance.

It pays producers directly, eliminates intermediaries, and sets prices through community agreement rather 
than speculative markets.

The margin that makes this possible, calculated: feeding 500 people costs $781,000 per year at market prices 
and $125,000 by paying producers directly. A factor of six to one — enough room to pay producers several times 
what they currently receive and still spend less.

Its infrastructure combines: assembly governance with double threshold, decentralized identity with verifiable 
and anonymous uniqueness, a social currency backed by real production, and an autonomous mesh network that 
operates without depending on commercial internet.


.


### 1. Project Description

#### 1.1 Vision and Mission

Vision: a world where access to food and basic resources depends not on market price but on community agreement 
and real production.

Mission: to build the coordination infrastructure that enables communities to self-manage their economy and 
governance, without intermediaries or dependence on external infrastructure.

#### 1.2 General Architecture
```
┌─────────────────────────────────────────────────────────┐
│  APPLICATION — interfaces, forums, social network,      │
│                translator                               │
├─────────────────────────────────────────────────────────┤
│  GOVERNANCE — assemblies, sortition deliberation,       │
│                channel-based agenda, identity           │
├─────────────────────────────────────────────────────────┤
│  ECONOMY — social currency, treasury, cooperatives,     │
│            concentration detection                      │
├─────────────────────────────────────────────────────────┤
│  LEDGER — chained with threshold signature (global)     │
│            + distributed ledgers with CRDTs (local)     │
├─────────────────────────────────────────────────────────┤
│  STORAGE — erasure coding, distributed custody,         │
│            periodic verification                        │
├─────────────────────────────────────────────────────────┤
│  NETWORK — LoRa (telegrams), HaLow (content),           │
│            BATMAN-adv (mesh routing)                    │
├─────────────────────────────────────────────────────────┤
│  HARDWARE — nodes, antennas, panels, batteries          │
└─────────────────────────────────────────────────────────┘
```
Governance layer. Community assemblies of around 150 people. Asymmetric double threshold. Deliberative panels 
by stratified sortition. Agenda determined by four channels with pure sortition in each.

Economic layer. Social currency as a ledger backed by real production. Common treasury with goods, 
infrastructure, and cooperatives. Accumulation ceiling and minimum hourly floor.

Ledger layer. Chained ledger with threshold signature for what requires global consensus — root identity,
treasury, global results, integrity anchors — and distributed ledgers with state convergence for everything else.

Network layer. LoRa for telegrams, votes, and alerts. Wi-Fi HaLow for content transport. BATMAN-adv for 
self-healing mesh routing. Community supernodes as soft hierarchy — accelerators, not requirements.


.


### 2. PROBLEM AND SOLUTION

#### 2.1 The Global Food Flow

All figures correspond to Berners-Lee, M., Kennelly, C., Watson, R., & Hewitt, C. N. (2018). Current global food
production is sufficient to meet human nutritional needs in 2050 provided there is radical societal adaptation. 
Elementa: Science of the Anthropocene, 6.Article 52, 2018, with 2013 data from FAO food balance sheets.
https://doi.org/10.1525/elementa.310


The crop account: all crops translated to kcal per person per day:
```
----------------------------------------------------------------------------------------------------------------
Directly edible crops produced                  5,935 kcal/person/day
Pasture and stover, not human-digestible        3,812 kcal/person/day
Total production                                9,747 kcal/person/day
Average energy requirement*                     2,353 kcal/person/day
Effectively eaten                               2,531 kcal/person/day
Real surplus                                    8%
----------------------------------------------------------------------------------------------------------------
```
* Global weighted average derived by the authors applying the methodology of the 2001 joint expert consultation 
on human energy requirements. Not a published figure: the original document provides tables by age, sex, weight, 
and physical activity.


The livestock account:
```
----------------------------------------------------------------------------------------------------------------
Edible crops fed to animals                     1,738 kcal
Pasture and stover fed to animals               3,812 kcal
Total consumed by animals                       5,550 kcal
Returned as meat, dairy and fish                  594 kcal
Conversion rate                                     12%
----------------------------------------------------------------------------------------------------------------
```
And the most striking figure from the study, on protein:

----------------------------------------------------------------------------------------------------------------
Protein eaten                                   81 g/person/day
Average requirement                             44 g/person/day
Excess consumption                              84%
Reduction in available protein by feeding
edible crops to animals                         51 g/person/day — 116% of global requirement
----------------------------------------------------------------------------------------------------------------


The study's own scenarios: stopping the practice of feeding edible crops to animals would be enough to 
adequately feed 9.7 billion people in 2050 without reducing waste or excessive consumption. Following the
projected trajectory would require 119% more production. This is a finding we cannot fully address ourselves, 
but which we wish to disseminate fully in the context of the present discussion.

And the conclusion the authors state: reducing waste and increasing yields are, in the absence of production 
increases, quantitatively less important than reducing the use of edible crops for animal feed.


## 2.2 Current Hunger

Source: FAO, IFAD, UNICEF, WFP, & WHO. (2026). The State of Food Security and Nutrition in the World 2026.- 
    -Rome. https://www.who.int/publications/m/item/the-state-of-food-security-and-nutrition-in-the-world-2026 

----------------------------------------------------------------------------------------------------------------
People unable to afford a healthy diet                  2.69 billion — 32.7%
People who faced hunger                                 645 million — 7.8%
Cost of a healthy diet, 2025                            $4.28 PPP/person/day
Same cost in 2021                                       $3.44
Same cost in 2017                                       $2.94
Increase in eight years                                 46%
African population unable to afford it                  66.6%
International extreme poverty line                      $3 PPP/day
----------------------------------------------------------------------------------------------------------------

The contrast the report itself highlights: the extreme poverty line is at $3, and eating healthily costs $4.28. 
The poverty line does not measure the ability to eat well — it measures the ability to survive poorly.


## 2.3 The Work of the Food System

Source: FAO, "FAO. (2025). Employment indicators 2000–2023 — July 2025 update. FAOSTAT Analytical Briefs, 
      No. 110. Rome. https://doi.org/10.4060/cd5821en 

----------------------------------------------------------------------------------------------------------------
People employed in agrifood systems, 2022               1.3 billion
Share of global employment                              Two out of every five employed people
Average weekly hours, 81 countries, 2023                40
Annual hours of the food system                         2.70 trillion    *Calculation: 1.3B × 40 × 52*
Hours per person per year                               330         *Calculation: 2.70T ÷ 8.2B* (total humanity)
Daily equivalent                                        0.90 hours       *Calculation: 330 ÷ 365*
----------------------------------------------------------------------------------------------------------------

Currently, the cost of feeding all of humanity healthily (the above studies translate the full range of all 
crops into calories)translates into each person in the world working one hour per day. Each person's daily
food would correspond to one hour of daily work. The figure includes people outside the workforce, such as
children and the elderly, but it is considered a strong reference indicator and will be used for future 
calculations — it is a calculation derived from two verified data points, not a published statistic. Its main 
caveat: the calculation assumes uniform working hours, and the source notes that hours fluctuate with planting
and harvest. The actual 
effective daily hours per person are probably lower, which reinforces the argument.

Why it matters: it establishes that the proposed minimum floor — one hour of work at least equal to one 
day's food — is materially achievable. It is not generosity: it is the proportion the system already has.

## 2.4 The Efficiency Factor

Source: USDA Economic Research Service.(2024). Food Dollar Series.Washington, DC.Corresponds to a single 
        country;treat as order of magnitude.
        https://www.ers.usda.gov/data-products/food-dollar-series

----------------------------------------------------------------------------------------------------------------
Producer share of total food spending                   11.8 cents per dollar
Share in supermarket purchases                          18.5 cents
Same figure in 1994                                     24 cents
What remains for crop producers after expenses          2.5 cents
Marketing cost                                          88.2 cents
----------------------------------------------------------------------------------------------------------------
The producer's share has halved in three decades.

The calculation applied to a community of 500 people:
----------------------------------------------------------------------------------------------------------------
Market price cost                          4.28 × 500 × 365        $781,000/year
Full-time equivalent workers               330 h × 500 ÷ 2,080 h   ≈ 80
Annual income per worker                   4.28 × 365              $1,560
Cost of paying producers                   1,560 × 80              $125,000/year
Factor                                     781,000 ÷ 125,000       ≈ 6 to 1
----------------------------------------------------------------------------------------------------------------

Three reasons explain it, and none is an efficiency of the project but rather an inefficiency of the current 
system: no payment for each link's commercial margin; no payment for the third that is wasted and incorporated 
into the price; no payment for long-distance transport.

Even paying double or triple the subsistence floor, the cost would still be half or less than buying the 
same food.

The assumption of 80 people is verified against peasant productivity data: the ratio of 6.25 people fed per 
worker falls within the documented range of 6 to 8 for small-scale agriculture.

## 2.5 The Solution

It does not propose producing more surplus, but rather that what is produced reaches people.

Direct payment to producers, eliminating the intermediation that captures 88% of the final price.

Prices set by community agreement, not by speculative markets.

Food delivered as a right and not sold — which eliminates from the root the need for anyone to work in degrading 
conditions to eat.

And a social currency as a ledger backed by real production, not as a speculative asset.

Sovereignty over resources: Adamas supports diversified local production, with local varieties, regenerative 
practices, and short delivery channels. Food sovereignty is not decreed: it is built from communities' control 
over their land, seeds, and water. Why? 1) Because a land's cultivation capacity is directly proportional to the 
health of an ecosystem whose plants include diverse native species. 2) Because the nutritional quality of crops 
grows equally proportionally to the above. Ethics is an important value for this study, but it will be argued 
with the relevant figures.

Infrastructure: it combines a chained ledger with threshold signature, distributed ledgers with CRDTs, and an 
autonomous communication network (LoRa + HaLow + BATMAN). Adamas is not an app on a centralized network: it is 
infrastructure that builds its own network and its own ledger.

The integrated proposal: the system closes the circle from the problem (sufficient production, poorly 
distributed) to the solution (direct payment, community agreement, autonomous network, assembly governance, 
economic and social circularity, and social currency with real backing). There are no loose pieces: each layer 
responds to a distortion in the current system.


.


## 3. TECHNICAL PROPOSAL

## 3.1 Governance

Neighborhood or zonal assemblies of around 150 people, with full autonomy over their affairs — self-determination
is relevant in organizing; it is a number at which organization does not become complicated. The network of 
organizations will make the difference.

Asymmetric double threshold for supra-local decisions, with safeguards against artificial fragmentation of zones.

Deliberative panels by stratified sortition, with broad random invitation and selection among those who accept. 
Compensation equivalent to the subsistence cost of the dedicated period — not as a benefit but as a condition of 
representativeness.

Agenda by four channels: pure sortition for 60% of seats, deterministic seniority queue for 20%, and 10% each 
for underserved zones and urgent matters. With seed generated by prior commitment among independent parties, 
so no one can choose the outcome.

Custodians at three independent levels — global, regional, local — with threshold signature, selection by 
stratified sortition, and staggered partial rotation.

### A Possible Permanent Pillar of Self-Governance: AdmsDID

AdmsDID is a decentralized identity system that enables each person to prove they are a single person without 
revealing which one, and without resorting to state credentials.

It operates in two layers: a root identity that never appears in transactions, and context-based derivations 
that prevent acting twice in the same domain — voting twice, receiving twice, accumulating beyond the ceiling 
— without allowing the linking of a person's actions across different domains. Attribute verification is done 
through zero-knowledge proofs: the system knows you meet the conditions, not who you are.

AdmsDID resolves the central tension of horizontal sovereignty participation: proving you are a single person 
without revealing which one.

In a system where each person has one vote and each person participates in the economy, the problem is not identity 
— it is uniqueness.

In governance: verifiable and anonymous participation, without dependence on state credentials, without exposure 
of personal data, and without possibility of duplication.

In economics: each person is one in the ledger of balances, no one can evade the accumulation ceiling with 
multiple identities, and the social currency reflects real work and production, not fictitious identities. 
The privacy of transactions is not an obstacle to equity; it is its condition.

The problem is not identity but uniqueness, and it is worth stating precisely: to prevent a person from 
registering twice, one must compare their registration against existing ones — and that comparison is 
exactly what anonymity would seem to prevent. 
Anonymity in global voting matters doubly because it prevents or undermines the verification of vote 
buying; the issue is that without a mechanism to prevent multiple registrations, both community voting 
and the distribution of social currency are vulnerable to duplication. Without external credentials, 
participation is out of reach for those who lack documents or do not wish to expose them. And we do not trust 
state registries or their records; we will not address the reasons for distrust: they are plain for all to see. 
We will mention that we consider state-verifiable credentials a security breach and understand that states' 
use of them lacks any ethics.

There is a reference implementation that resolves the duplication/deduplication tension: Janus, presented at 
the IEEE Symposium on Security and Privacy in 2024 and developed by the CISPA center together with the SPRING 
group of the École Polytechnique Fédérale de Lausanne and the International Committee of the Red Cross. Its 
code is open source and was designed for privacy-preserving biometric deduplication in humanitarian identification 
programs. Before continuing, we note that this text opposes invasive biometrics, particularly ocular registration; 
if biometrics become necessary due to circumstances, it must be a registration generated by free
people for free people, at their voluntary decision.

Janus enables comparing a registration against a set without any party being able to read its content. The 
computation is distributed among multiple custodians and returns a single bit: there is a match or there is not.

On top of that, the project adds its own architectural decision: the regionally federated corpus.

Janus resolves private comparison; limiting the scope of comparison is what makes the scaling problem tractable. 
A single planetary biometric registry is not viable with any available technology — the rate of ambiguous cases 
grows with the size of the set until it becomes complex, although the formulation of using low-invasive and 
additive biometrics — we propose showing our hands: palm vein registration via scanner plus fingerprints, 
combined with the necessary open public community attendance of the registration, and complementary biometrics 
in cases of need to avoid ableist biases — is viable. With regional corpora and encrypted cross-region 
queries, the number becomes manageable through human review.

A terminological clarification worth establishing: the corpus exists and is comparable — that is its function. 
What does not exist is a corpus readable by a single party. The distinction is not between having a registry
and not having one, but between one that an individual actor can read and one that no party can read alone.

In early stages, uniqueness — an approximation to uniqueness — is maintained through another route: registration 
at public events with cross-verification between neighboring communities, random sampling of rosters, and the 
knowledge each assembly has of its own members. 
It is less precise and is what works without infrastructure, relying on the will of the people.

And a decision worth declaring: the system does not depend on verified uniqueness to operate. Areas that cannot 
deploy the federated corpus infrastructure are predictably the most vulnerable — making it a participation 
requirement would exclude them.

A declared caveat: the documented evaluation of Janus corresponds to programs on the order of tens or hundreds 
of thousands of people. 
Statistics show it is viable, however.


## 3.2 Economy

Social currency: a ledger, not a speculative asset. It does not trade on any market, is not acquirable outside 
the system, and its value does not float according to expectations.

Its backing is existing productive capacity — land, infrastructure, cooperatives (+social-purpose cooperatives 
of the treasury). Not a promise of conversion.

And from this comes a property that no monetary backing has: it cannot be run on. No one can demand it all be 
converted to something else, because it is not a claim right but the medium of exchange of an economy that 
produces.

The common treasury operates as a bridge to the outside. It buys abroad with its reserves, sells abroad what
it produces, and credits internally. There is no verifying contract or conversion mechanism between 
ledgers — there is an entity that transacts in both worlds.

Accumulation ceiling (air ceiling or fixed), with staggered notification, not erosion: those who exceed the 
threshold receive notices with a deadline inversely proportional to the amount, and the idle surplus returns 
to the fund for traceable reinvestment. It is up to the detector — under the necessary assisted fine-tuning 
for the early stages — to decide when the economy should send threshold warnings.

Concentration detection by arithmetic with fixed parameters. No machine learning, no neural networks.

## 3.2.1 The Treasury: Assets, Wallet, and the Two Stages of Adamas

The Treasury is not an abstract fund: it is physical and digital patrimony.

On one hand, physical assets — land, infrastructure, social cooperatives, machinery, stocks — that constitute 
the productive base of the system. They are the real guarantee that the social currency is not a promise but 
the reflection of an economy that produces.

On the other hand, an investment wallet — digital assets, fiat, and liquid reserves — that allows the Treasury 
to operate in the outside world: buying technology, inputs, and everything the circuit does not produce, 
without needing bridges or exposing the social currency to external volatility.

This duality is what makes the two-stage model possible.

### Stage 1: Growth and Construction

The Treasury concentrates decision-making, reserve management, and cooperative coordination. It is the stage 
of initial investment, fine-tuning of parameters — conversion rate, accumulation ceilings, minimum hourly 
floor — and infrastructure deployment. Without this centralized stage, there is no economy to sustain: a 
currency that buys nothing is worth nothing, and a circuit without internal supply does not circulate.

Fine-tuning here is an ongoing task: the conversion rate is periodically reviewed, ceilings are calibrated 
according to real production, and economic parameters adapt to the experience of the first communities. 
It is not improvisation: it is learning before scaling.

The fund's adjustments must be decoupled from the treasury and automated through arithmetic and the detector, 
gradually and increasingly.

### Stage 2: Autonomy and Transfer

When the system reaches a high level of participation, when the internal economy is autonomous and stable, 
and/or when AdmsDID guarantees that each person is one without revealing their identity, the Treasury transfers 
its main function to the community.

The transfer is not a renunciation: it is the condition of the system's maturity, and in its transfer several 
factors will be considered, such as community votes, the number of participants needed for a healthy economy, 
and the voluntary implementation of AdmsDID.

The governance of economic parameters passes to the assembly. Treasury management is distributed among 
custodians. The social currency ceases to be administered and becomes governed. The Treasury then becomes a
common patrimony without an owner — land, infrastructure, and social-purpose cooperatives — that the community 
administers collectively.

Fine-tuning, at this stage, is no longer necessary: the economy regulates itself through agreement among peers, 
not through the calibration of a central administrator.

AdmsDID is a protocol that would make this transition possible and easy. Without unique and verifiable identity, 
community voting would be vulnerable to duplication. Without zero-knowledge proofs, participants' sovereignty 
would be nominal. With AdmsDID, the community can decide globally; without AdmsDID, organization is forced to 
be regional, although palliative measures have also been taken in this area.


## 3.2.2 Detector

The detector is an arithmetic monitoring system, not a surveillance system.

It does not observe people or content. It observes flows of social currency in the ledger. It does not know 
who is who. It only knows how much moves, between which accounts, and with what pattern.

Its function is to detect anomalous concentration and multi-account mass release attacks, without the need 
for human surveillance or machine learning.

It distinguishes between a legitimate mass purchase — seasonal pattern, accounts with contribution history, 
funds circulating within the circuit — and an attack — newly created accounts with no history, funds 
concentrated in few recipients, or leaving the circuit toward external conversion.

The detector only signals anomalies. It decides nothing. The decision is always the community's.


## 3.3 Networks

LoRa: telegram layer. Votes, cryptographic fingerprints, alerts. 2 to 5 kilometers in urban settings, 
          tens of kilometers in line of sight. A signed vote fits in less than a kilobyte.

Wi-Fi HaLow: content transport. 800 meters with line of sight according to field measurements. 
          The discrepancy with manufacturers' published figures is registered as pending field verification.

BATMAN-adv: mesh routing, layer 2, self-healing, in production for over a decade.

Community supernodes as soft hierarchy — they accelerate the network without being a requirement 
          for its operation.

Conflict-free state convergence for operation in partitioned networks: nodes converge upon reconnection 
          without needing consensus.

## 3.4 Programming

Core in Rust: identity, post-quantum cryptography, verification, state convergence, protocol.

The separation criterion: the core handles what manages secrets and what must run on all platforms. 
            A memory error in the interface crashes the application; in the cryptographic layer 
            it leaks a key.

Peripherals in what is already proven to work: routing in C, radio firmware in C++, interfaces in 
            each platform's native language.

Chained ledger, not an external chain framework. Frameworks with a main-chain architecture were 
            evaluated and discarded: they require renting space with permanent cost in foreign 
            currency, operate with validators that are not one's own, and their governance is by 
            economic participation — contradicting the one-person-one-vote principle.

Reproducible builds mandatory from the start. The same source must produce the same binary, verifiable by anyone.

## 3.5 Security

No bridges between chains. This is the most important security decision of the design: bridges concentrated 69% 
of the sector's stolen funds in 2022, and the largest incident of 2026 — $292 million — occurred due to a 
verification scheme with a quorum of one over one.

Threshold signatures with distributed key generation for critical decisions. No individual party can authorize 
anything.

Identity recovery through three concurrent paths: key fragmentation among chosen guardians, seed phrase, and 
assembly re-enrollment.

Frequent fragment refresh, infrequent people rotation. Refresh invalidates compromised fragments without exposing 
the system to the moment of greatest vulnerability, which is the complete renewal of the set.

Node updates signed by threshold, distributed through the mesh itself, with verification before applying, ability
to revert, and staggered deployment. No silent updates — this is the direct lesson from the history of malicious 
extensions, where the main vector was not installation but automatic updates.

And the figure that orders security priorities: 88% of the sector's losses in 2025 came from private key 
compromise, not code errors. One case lost $285 million after six months of social engineering. There was no 
exploit: there was patience.


.


## 4. Integration with World Mobile

### AirNodes as access nodes.

They provide connectivity to Adamas users in areas with coverage. There is no technical dependency: it is
shared use of transport infrastructure.

Possible auxiliary functions, with strict conditions:
--------------------------------------------------------------------------------------------------------------
Content caching         It is cache, not custody. Content can be lost without affecting the system.
Network entry point     Provides access to those without their own node. Does not participate in the mesh.
Content indexing        Accelerates searches. It is an improvement, not a dependency.
--------------------------------------------------------------------------------------------------------------

The distinction between cache and custody is what makes this integration possible. Cache accelerates access to 
content that exists elsewhere; custody is the responsibility for that content's existence. Adamas nodes custody; 
AirNodes can accelerate.

On technical implementation and its security condition. If an AirNode operator wishes to run auxiliary functions, 
they would do so through a lightweight, read-only, keyless component. It handles no secrets, signs nothing, 
decides nothing. It serves pre-signed content, whose integrity the receiver verifies against its cryptographic
hash. If compromised, it would serve invalid content that the receiver discards — it cannot inject valid content
because it has nothing to sign it with. This condition is what makes it acceptable for Adamas-related software 
to run on hardware we do not control.

### On EarthNodes:

Limited functions, without custody or validation.

They cannot be used for archive custody or validation.

Adamas archive nodes custody the system's historical record — minutes, decisions, identities — through erasure 
coding among nodes of the network itself, with periodic cryptographic verification that each custodian retains 
their fragment. Delegating this to third-party infrastructure breaks the architecture, because custody 
verification loses meaning if the custodian does not integrate with the system. Adamas communities' autonomy 
depends on autonomy in their infrastructure; possible incompatibilities in infrastructure and programming 
architecture are also a matter for analysis.

Validation is discarded for a different reason: concentrating verification in a set of external nodes creates 
exactly the single point of compromise that the design avoids. The largest security incident in the sector in 
2026 occurred due to a verification scheme with insufficient quorum.

What they can do, under the same non-criticality condition:
-------------------------------------------------------------------------------------------------------------
Bounded computation         Not involving sensitive data or keys. Translation processing, 
                            batch signature verification, indexing.
Temporary storage           Cache, never permanent custody.
Network entry point         Access for those without their own node.
-------------------------------------------------------------------------------------------------------------

Their computing capacity is greater than an AirNode's, making them suitable for tasks requiring processing 
without responsibility. Integrations with EarthNodes are under analysis; similarly, functions that Adamas 
can fulfill for them will be evaluated to encourage collective participation.

### On WMTX

What can be offered: that the Adamas treasury accepts WMTX as a form of purchase or contribution, with a 
preferential exchange rate for social currency. This gives WMTX real utility outside its own ecosystem, 
without exposing either ledger. Due to the nature of the social currency and economic architecture, we cannot 
offer ledger integration or bridges. 

### What Adamas Offers to Node Operators

Verifiable contribution certificate. An AirNode or EarthNode operator who contributes capacity to the Adamas 
network can obtain a verifiable accreditation as community support infrastructure. It is public and traceable 
recognition, not an asset or a right. It does not grant governance or economic reward, but it does record 
participation in the early stages of a network destined for ecosocial well-being.

They can reside in the distributed ledgers and not in the chained ledger. That ledger is deliberately kept 
minimal — root identity, treasury, global results, integrity anchors — and adding certificates would add 
unnecessary load. In distributed ledgers, it remains verifiable by anyone.

Access to the platform as any participant. An operator can use forums, inform themselves, and participate 
in the circuit like any person.

What is not offered, and should be stated with its rationale:

    Vote on the platform. Participation in decisions corresponds to verified people, not just someone who 
    operates infrastructure. A node is not a person, but that does not prevent those people from integrating 
    into their community or into Adamas.

    Reward in social currency. Social currency rewards participation in the productive circuit. Paying it 
    to external nodes would break the model.

### What Is Offered to World Mobile: Reciprocity — Access to the Adamas Mesh

World Mobile users could access the Adamas mesh network where there is no AirNode coverage, or where it 
is deficient. It is an exchange of complementary infrastructure: World Mobile provides high-speed internet 
where its network reaches; Adamas provides autonomous long-range communication where no network reaches.

-------------------------------------------------------------------------------------------------------------
Range                       Low-speed messaging — telegrams, text, alerts.
Priority                    Community participants have precedence; external access uses remaining capacity.
No economic exposure        Network access does not imply access to social currency or governance.
No dependency               The mesh exists and functions independently of this opening
-------------------------------------------------------------------------------------------------------------

On priority, and it is a technical condition, not a preference: long-range radio bands have regulatory duty 
cycle limits — how long a device can transmit per hour, depending on jurisdiction. Opening the mesh without 
constraints could saturate the spectrum available to communities, which is the use the mesh exists to serve. 
Low-priority external access preserves the offering without compromising the main function: the 
self-organization of people in the territory, which is what justifies this project.

In the future, for Adamas it is a logistical necessity to invest in antennas and decentralized fiber to 
connect areas with aerial link difficulties, in an auxiliary manner and custodied by nodes, adding speed 
and resilience to the network.It is also imperative to make the mesh networks of the various scales 
sufficiently dense.


.


## 5. Roadmap

Phase 1 — six months. Functional prototype of assembly governance and social currency ledger. LoRa nodes 
                      operational in a pilot community. Field verification of HaLow's real range.

Phase 2 — twelve months. Deployment in a rural-urban pair. First cooperatives operating before releasing the
                      social currency — a currency that buys nothing is worth nothing. Food circuit in operation.

Phase 3 — twenty-four months. Scaling to a regional network. Chained ledger operational with custodians at 
                      three levels. Integration with AirNodes where coverage exists.

Phase 4 — thirty-six months. Multinational network. The minimum viable scale is several countries with productive 
                      complementarity — no country has sufficient caloric area for its own population.

And a precision about order that should be stated: the first deployment should not be an isolated rural community. 
                      A community alone has no one to exchange with and its currency becomes immobile. It must be 
                      a rural-urban pair from the start.

.


## 6. Budget and Milestones

### 6.1 Annual Platform Cost in Initial Operational Stage
--All components are design assumptions, not operational data. 
Compensation is calculated at the subsistence minimum.--

-----------------------------------------------------------------------------------------
Custody of 20 supernodes                   20 × 40 × 12                        9,600
Custody of 50 historical nodes             50 × 15 × 12                        9,000
Deliberation, 10 annual panels             10 × 20 × 18 days × 4.28            15,410
Development, 5 people                      5 × 800 × 12                        48,000
Non-personnel infrastructure               Connectivity, energy, replacement   12,000
Total                                                                          94,010
-----------------------------------------------------------------------------------------
Development is half the cost and does not scale with participants — it may costs the same with 600 users 
as with 60,000.


### 6.2 Self-Sufficiency
```
-----------------------------------------------------------------------------------------
Volume generated per participant          1,560 × 5 circulation turns        7,800
Fund commission, 1%\*                     7,800 × 0.01                      78
Participants needed                       94,010 ÷ 78                       ≈ 1,205
-----------------------------------------------------------------------------------------
```
* Merely a reference calculation; lower commissions are intended.

With about 600 active people, the platform pays for itself. In the pessimistic scenario — low commission 
and slow circulation — about 2,000 are needed.

The most fragile assumption is the five circulation turns, which depend on the existence of internal supply. 
In the early stages, there will be little.

### 6.3 Capital of the Food Circuit
```
-----------------------------------------------------------------------------------------
Land leasing                   15–25 million                    $230–$380
Land acquisition                150–250 million                  $2,300–$3,800
-----------------------------------------------------------------------------------------
```
Only acquisition in the treasury builds global common patrimony. Leasing pays rent to whoever owns the land.

Reference: a 10,000-hectare operation feeds between 50,000 and 80,000 people if production is directed to direct
human consumption, with 30 to 50 workers.


### 6.4 Minimum Amount Requested and Breakdown

$150,000 is requested for twelve months, corresponding to Phase 1 complete and the start of Phase 2.

#### Design for 200 People, 20 Community Nodes

One node per ten people. Multi-use nodes are not simple radios: they combine communication, local storage, wireless
access point, and autonomous energy.

Community Multi-Use Nodes — 20 Units
----------------------------------------------------------------
Single-board computer, 4 GB                            70
Storage, industrial card or SSD 256 GB                 30
LoRa module with base board                            59
5 dBi outdoor antenna with cable                       35
20 W solar panel, 20 Ah battery, controller            100
IP67 waterproof enclosure                              25
Mounting, cabling, miscellaneous                       20
Subtotal per node                                      339
20 nodes                                               6,780
----------------------------------------------------------------

Community Supernodes — 3 Units
----------------------------------------------------------------
Higher-capacity computer                           500
2 TB storage                                       120
HaLow radio with directional antenna               200
LoRa gateway                                        59
100 W solar panel, 100 Ah battery, controller      400
Enclosure, electrical protection                   140
Subtotal per supernode                           1,419
3 supernodes                                     4,257
----------------------------------------------------------------

Historical Archive Node — 1 Unit
----------------------------------------------------------------
Higher-capacity compute equipment          800
Redundant storage, 2 × 4 TB                300
Extended autonomous energy                 450
Protection and backup                      120
Subtotal                                   1,470
----------------------------------------------------------------


Complementary Items
----------------------------------------------------------------
Solar HaLow repeaters, 2 units                           500
Portable nodes for those without phones, 20 units        1,000
Installation and measurement tools                       300
Spare parts, 15% of hardware                             270
Total                                                    1,530
----------------------------------------------------------------

Total
----------------------------------------------------------------
Hardware                                        14,037
Shipping and import, ~25%                        3,509
Total                                           17,546
----------------------------------------------------------------
Remains within the 20,000 budget with a margin of about $2,400.

Infrastructure and Operations
----------------------------------------------------------------
Link connectivity, 12 months                    600
Development services and domains                1,200
Field failure replacement                       2,500
Transport and field installation                3,000
Local operator training                         2,000
Maintenance tools                               1,500
Backup energy                                   500
Field contingency                               1,000
Unforeseen                                      1,700
Total                                           14,000
----------------------------------------------------------------

*Annexed: Scalability Figures
----------------------------------------------------------------
Network cost per person, first zone                  $95
Marginal cost per additional person in same zone     ~$34
Cost per multi-use community node                    $339
----------------------------------------------------------------
The difference between these figures is what matters for scaling.
The $95 includes supernodes and archive, which are fixed costs of the zone.
Doubling the population of that zone does not double the cost: it only adds 
community nodes, at $339 per ten people.
With 2,000 people in the same zone, the cost per person would fall to about $45.*


#### Budget Breakdown — Requested Amount
----------------------------------------------------------------------------------------------
Project direction                24,000                $2,000/month, full-time dedication
Core development                192,000                Two people, $8,000/month each
Pilot hardware                   20,000                LoRa nodes, HaLow, supernodes, energy
Infrastructure and operations    14,000                Connectivity, services, replacement
Reserve                          20,000                General unforeseen
                                 –20,000               Rounding adjustment
Total                           250,000
----------------------------------------------------------------------------------------------
The strategy is test before scaling. Complete system development would require significantly more, but we 
expect to achieve some degree of circularity, or to make further applications with device proof.

This amount covers what is needed to demonstrate that the mechanism works: an operational prototype of assembly
governance and social currency ledger, with nodes deployed in a pilot community and field verification of 
network assumptions. The estimated timeframe is one year.


#### Full estimate to reach stability in three regions: 3.2 million USD over 36 months
--------------------------------------------------------------------------------------------------------------
Category                                  Amount          Detail
Software development                      540,000      3 years, growing from 2 to 5 developers
Project direction and coordination        108,000      3 years
Network hardware, three regions           180,000      ~60,000 per region: supernodes, access nodes,archive 
                                                       nodes, antennas, solar
Productive land acquisition               1,200,000    Enters the treasury permanently and is never resold
Agricultural equipment and logistics      400,000      Machinery, transport, storage, cold chain
Working capital, food circuit             450,000      First production cycle, which by definition cannot 
                                                       self-finance
Cooperative seed funding                  200,000      Non-food cooperatives — repair, tools, textiles, 
                                                       construction
Security audits                           60,000       Cryptography, threshold signatures, reproducible builds
Legal and jurisdictional structure        40,000       Entity formation across three jurisdictions
Contingency                               22,000
Total                                     3,200,000
--------------------------------------------------------------------------------------------------------------


### 6.5 Measurable Milestones

----------------------------------------------------------------------------------
| Phase | Month | Verifiable Milestone                                           |
|-------|-------|----------------------------------------------------------------|
|   1   |   3   |  Identity ledger operational in test environment               |
|   1   |   6   |  Functional prototype: assembly, voting, and balance ledger    |
|   2   |   9   |  LoRa nodes deployed and operational in pilot community        |
|   2   |  12   |  Field measurement of HaLow's real range                       |
|   2   |  12   |  First cooperatives operating before releasing social currency |
|-------|-------|----------------------------------------------------------------|
----------------------------------------------------------------------------------

Each milestone is verifiable by third parties, not by self-declaration.


.




##Annexes

### Annex A — System Architecture
### A.1 Layers
```
┌───────────────────────────────────────────────────────────┐
│  APPLICATION                                              │
│  Interfaces · Forums · Social network · Translator        │
├───────────────────────────────────────────────────────────┤
│  GOVERNANCE                                               │
│  AdmsDID · Assemblies · Sortition deliberation            │
│  Channel agenda · Asymmetric double threshold             │
├───────────────────────────────────────────────────────────┤
│  ECONOMY                                                  │
│  Social currency · Common treasury · Cooperatives         │
│  Concentration detection · Minimum hourly floor           │
├───────────────────────────────────────────────────────────┤
│  LEDGER                                                   │
│  Chained with threshold signature (global consensus)      │
│  Distributed ledgers with CRDTs (local state)             │
├───────────────────────────────────────────────────────────┤
│  STORAGE                                                  │
│  Erasure coding · Distributed custody                     │
│  Periodic cryptographic verification                      │
├───────────────────────────────────────────────────────────┤
│  NETWORK                                                  │
│  LoRa (telegrams) · HaLow (content)                       │
│  BATMAN-adv (mesh routing)                                │
├───────────────────────────────────────────────────────────┤
│  HARDWARE                                                 │
│  Nodes · Antennas · Solar panels · Batteries              │
└───────────────────────────────────────────────────────────┘
```
### A.2 Node Hierarchy
```
                    ┌──────────────────┐
                    │  HISTORICAL NODE │
                    │  Archive custody │
                    └────────┬─────────┘
                             │
              ┌──────────────┴──────────────┐
              │                             │
     ┌────────▼─────────┐         ┌─────────▼────────┐
     │   SUPERNODE      │◄───────►│   SUPERNODE      │
     │   COMMUNITY      │  HaLow  │   COMMUNITY      │
     │                  │         │                  │
     │  Storage         │         │  Storage         │
     │  Translator      │         │  Translator      │
     │  Routing         │         │  Routing         │
     └────┬────────┬────┘         └────┬─────────────┘
          │        │                   │
      LoRa│    WiFi│               LoRa│
          │        │                   │
    ┌─────▼──┐  ┌──▼─────┐       ┌─────▼──┐
    │ ACCESS │  │ ACCESS │       │ ACCESS │
    │ NODE   │  │ NODE   │       │ NODE   │
    └────────┘  └────────┘       └────────┘
       │              │
   ┌───▼───┐     ┌────▼───┐
   │Person │     │ Person │
   └───────┘     └────────┘
```
The hierarchy is soft: supernodes accelerate the network; they are not
a requirement for its functioning. If a supernode falls, access nodes 
continue to communicate with each other.

### A.3 Economic Circuit Flow
```
   EXTERNAL CAPITAL
   (contributions, sale of production, MS purchases)
          │
          ▼
   ┌─────────────┐
   │   TREASURY  │  External reserves + assets + cooperatives
   │             │  Threshold signature · Total transparency
   └──┬───────┬──┘
      │       │
      │       └──────────► PURCHASE ABROAD
      │                     (technology, machinery, inputs)
      ▼
   PAYS IN SOCIAL CURRENCY
   to those who produce, transport,
   stockpile, and custody nodes
      │
      ▼
   ┌──────────────────────────────────┐
   │  INTERNAL CIRCUIT                │
   │                                  │
   │  People ──spend──► Cooperatives │
   │     ▲                      │     │
   │     │                      │     │
   │     └───pay work───────────┘     │
   │                                  │
   │  Each exchange leaves a commission ─┼──► FUND
   └──────────────────────────────────┘
      │
      ▼
   FOOD DELIVERED
   (not sold — it is a right, not merchandise)
```
### A.4 Initial Integration with World Mobile
```
   ┌─────────────────────┐         ┌──────────────────────┐
   │   WORLD MOBILE      │         │      ADAMAS          │
   │                     │         │                      │
   │  ┌───────────┐      │         │   ┌──────────────┐   │
   │  │ AirNodes  │──────┼─────────┼──►│ Users        │   │
   │  │           │  connectivity  │   │ with access  │   │
   │  └───────────┘      │         │   └──────────────┘   │
   │                     │         │                      │
   │  ┌───────────┐      │         │   ┌──────────────┐   │
   │  │ EarthNodes│──────┼─────────┼──►│ Cache        │   │
   │  │           │   aux computing│   │ Indexing     │   │
   │  └───────────┘      │         │   └──────────────┘   │
   │                     │         │                      │
   │  ┌───────────┐      │         │   ┌──────────────┐   │
   │  │  WMTX     │──────┼─────────┼──►│ Treasury     │   │
   │  │           │    possible    │   │ (reserves)   │   │
   │  └───────────┘      │ purchase│   └──────────────┘   │
   │                     │         │                      │
   │  ┌───────────┐      │         │   ┌──────────────┐   │
   │  │ Users     │◄─────┼─────────┼───│ Mesh network │   │
   │  │ without   │   autonomous   │   │ LoRa + HaLow │   │
   │  │ coverage  │   communication│   └──────────────┘   │
   │  └───────────┘      │         │                      │
   └─────────────────────┘         └──────────────────────┘
```
* No bridges between ledgers*

* No cross-validation*

* No delegated custody*

* Each network functions without the other... but together they work much better.*



### Annex B — Data Tables

### Tables from the Main Text and Annexes

 ### B.1 Global Food Flow
----------------------------------------------------------------------------------

Directly edible crops produced                  5,935 kcal/person/day
Pasture and stover, not human-digestible        3,812 kcal/person/day
Total production                                9,747 kcal/person/day
Average energy requirement                      2,353 kcal/person/day
Effectively eaten                               2,531 kcal/person/day
Real surplus                                    178 kcal → 8%
----------------------------------------------------------------------------------
----------------------------------------------------------------------------------

Total consumed by animals                       5,550 kcal/person/day
Returned to human chain                         594 kcal/person/day
Conversion rate                                 12%
----------------------------------------------------------------------------------

Protein:
----------------------------------------------------------------------------------
Protein eaten                                   81 g/person/day
Recommended average requirement                 44 g/person/day
Excess consumption                              84%
Reduction in available protein by feeding
edible crops to animals                         51 g — 116% of global requirement
----------------------------------------------------------------------------------

### B.2 Hunger and Food Cost

----------------------------------------------------------------------------------
People unable to afford a healthy diet           2.69 billion — 32.7%
People who faced hunger in 2025                  645 million — 7.8%
Cost of a healthy diet, 2025                     $4.28 PPP/person/day
Same cost in 2021                                $3.44
Same cost in 2017                                $2.94
Increase in eight years                          46%
International extreme poverty line               $3 PPP/day
African population unable to afford it           66.6%
----------------------------------------------------------------------------------

### B.3 Work of the Food System

----------------------------------------------------------------------------------
People in agrifood systems, 2022                1.3 billion        Verified
Share of global employment                      Two out of five    Verified
Average weekly hours, 81 countries              40                 Verified
Annual system hours                             2.70 trillion      Calculation
Hours per person per year                       330                Calculation
Daily equivalent                                0.90 hours         Calculation
----------------------------------------------------------------------------------

### B.4 Producer Share in Price

----------------------------------------------------------------------------------
Share of total food spending, 2024                   11.8 cents per dollar
Share in supermarket purchases                       18.5 cents
Same figure in 1994                                  24 cents
What remains for crop producers after expenses       2.5 cents
Marketing cost                                       88.2 cents
----------------------------------------------------------------------------------

### B.5 Efficiency Factor

----------------------------------------------------------------------------------
Market price cost, 500 people               4.28 × 500 × 365        $781,000/year
Full-time equivalent workers                330 h × 500 ÷ 2,080 h   ≈ 80
Annual income per worker                    4.28 × 365              $1,560
Cost of paying producers                    1,560 × 80              $125,000/year
Factor                                      781,000 ÷ 125,000       ≈ 6 to 1
----------------------------------------------------------------------------------

### B.6 Industrial Scale

----------------------------------------------------------------------------------
Reference area                                    10,000 hectares
People working                                    30 to 50
People fed, direct human consumption              50,000 to 80,000
People fed, current model                         15,000 to 25,000
Calories reaching humans                          30 to 40%
----------------------------------------------------------------------------------

### B.7 Security Failure Precedents

----------------------------------------------------------------------------------
Proportion stolen in cross-chain bridges, 2022                   69%
Largest bridge loss, 2026                                        $292 million
Proportion of losses from key compromise, not code errors        88%
Loss from six-month social engineering                           $285 million
Collapse of algorithmic stabilization mechanism, 2022            ≈ $40 billion
----------------------------------------------------------------------------------


.



## Annex C — Glossary

AdmsDID          Decentralized identity system of the project. Enables proving one is a single person without 
                 revealing which one and without resorting to state credentials.

AirNode          World Mobile network internet access point.

BATMAN-adv       Layer 2 mesh routing protocol that self-heals upon node failure. In production for over a 
                 decade.

Erasure coding   Technique that divides a file into fragments with mathematical redundancy, so that only a 
                 fraction is needed for full reconstruction. More efficient than full copy replication.

CRDT             Conflict-free Replicated Data Type. Data structure that allows multiple copies to converge to 
                 the same state without requiring coordination or consensus. Enables operation in partitioned 
                 networks.

Custodian        Person or entity that holds a fragment of a cryptographic key. No one can sign alone.

DID              Decentralized Identifier. Identifier that does not depend on an issuing authority.

EarthNode        World Mobile network validation and coordination node.

Threshold signature Scheme         the key is distributed among multiple custodians and the concurrence of a 
                 minimum number is required to sign. The full key never exists anywhere.

Janus            Privacy-preserving biometric deduplication protocol. Enables comparing a registration against 
                 a set without any party being able to read its content; returns a single bit.

LoRa             Long-range, very low-bitrate radio technology. Suitable for short messages over tens of 
                 kilometers with minimal consumption.

Social currency  Internal circuit exchange unit. Does not trade, is not acquirable outside the system, does not
                 multiply itself, and does not buy essentials.

Nullifier        Value derived from an identity that prevents acting twice in the same domain without revealing 
                 who it is or allowing linking across different domains.

Minimum hourly floor Value         Below this no hour of work may be agreed within the system.

Zero-knowledge proof (ZK)          Cryptographic method enabling proof that a condition is met without revealing 
                 the information that satisfies it.

Chained ledger   Ordered record where each block references the previous one by its cryptographic hash, signed 
                 by a threshold of custodians. Not a blockchain with economic consensus: no mining, no token 
                 to sustain security, no programmable contracts.

Community supernode                Node with greater storage and computing capacity that accelerates the network
                 of a zone. Soft hierarchy: its failure does not impede functioning.

Air ceiling      Accumulation limit mechanism. Those exceeding the threshold receive notices with a deadline 
                 inversely proportional to the amount; the idle surplus returns to the fund for traceable 
                 reinvestment. The risk margin is determined by the detector according to the economy.

Common treasury  Ownerless patrimony: land, infrastructure, and social-purpose cooperatives. Operates as a bridge
                 to the outside by buying and selling, and credits social currency internally.

Wi-Fi HaLow      Wi-Fi variant in the sub-1 GHz band, with greater range and lower rate than conventional Wi-Fi.



.



## References


Berners-Lee, M., Kennelly, C., Watson, R., & Hewitt, C.N. (2018). "Current global food production is sufficient to meet human nutritional needs in 2050 provided there is radical societal adaptation." Elementa: Science of the Anthropocene, 6:52. https://doi.org/10.1525/elementa.310

FAO (2025). Employment indicators 2000–2023 — July 2025 update. FAOSTAT Analytical Briefs, No. 110. Rome. https://doi.org/10.4060/cd5821en

FAO, IFAD, UNICEF, WFP, & WHO (2026). The State of Food Security and Nutrition in the World 2026. Rome. https://doi.org/10.4060/cd8306en

World Inequality Lab (2026). World Inequality Report 2026. Paris. https://wir2026.wid.world

USDA Economic Research Service (2024). Food Dollar Series. Washington. https://www.ers.usda.gov/data-products/food-dollar-series/

WHO, FAO, & United Nations University (2001). Human Energy Requirements: Report of a Joint Expert Consultation. Rome. https://agris.fao.org/search/en/records/647396acce9437aa760043c0

EAT-Lancet Commission (2025). Reference for healthy diet of 2,500 kcal daily (2025 update). https://eatforum.org/eat-lancet/

Janus — Privacy-preserving biometric deduplication protocol. IEEE Symposium on Security and Privacy, 2024. CISPA, SPRING group of EPFL, and International Committee of the Red Cross. Code available in public repository. https://eprint.iacr.org/archive/2023/1377/1699444969.pdf

