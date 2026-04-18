# Kansas City Chiefs Offensive Play Calling Strategy 

## Project Overview
The Kansas City Chiefs have been an annual Super Bowl contender over the past eight years, built around head coach Andy Reid's offensive mind and quarterback Patrick Mahomes. Sustained success at that level, however, has forced the Chiefs to continually evolve their offensive strategy as defensive coordinators across the league adjust to stop them. Winning becomes more difficult when every opponent has full access to the same film and data. In this case, analytics applied well, can extend a team's competitive edge in a sport that is already deeply data centric.

This project focuses on offensive play-calling strategy, specifically, how the Chiefs can use data to identify the most effective plays, formations, and personnel groupings against different defensive alignments. Modern NFL defenses deploy a wide range of fronts and coverages — 4-3, 3-4, nickel, dime, and various hybrid packages — and the ability to diagnose and attack each look is a significant competitive advantage. The tool would provide data driven recommendations on pass concepts against specific defensive fronts.

## Decision-Making Problem
The decision this tool supports is: **"Given the defensive front, coverage look, and situation we are about to face, what play concepts, motion usage, and run schemes have produced the highest expected value and how does our own tendency compare to league wide leaders in the same situations?"** This affects weekly game planning, the structure of the call sheet, in game adjustments, and the self scouting process used to ensure the Chiefs are not falling into predictable patterns that opposing defensive coordinators can exploit.

## Proposed Analytics Approach
The analysis would use NFL play by play data (nflfastR) for league wide context and, where available, charted data from sources such as PFF or Next Gen Stats for defensive front, coverage, personnel, and motion details. The tool would divide plays by down, distance, field position, defensive front (4-3, 3-4, nickel, dime), and coverage (single-high, two-high, man, zone), then evaluate play concept effectiveness using expected points added (EPA), success rate, and explosive play rate. 

## Use by Decision Makers
The primary users are **head coach Andy Reid** and the offensive coordinator during the weekly game plan. Quality control coaches would run the tool during film study to prepare a defense specific recommendation sheet, which Andy Reid and the OC would use to shape the pass concept tree, motion package, and run menu for that week's opponent. O

## Connection to Chapter 7
This idea currently sits in the **creative phase** of Alamar's innovation framework. The decision problem has been stated, the data sources and analytical approach have been identified, and the intended users and workflow are defined. However, no prototype has been built, no coach has interacted with a mockup, and no feedback loop exists with the football operations staff. According to Chapter 7, the next step is prototyping. 

## Prototype Enhancement
The original project scoped recommendations around three dimensions: pass concepts against defensive fronts, pre snap motion usage, and run scheme selection. The proposed enhancement adds a **self-scouting tendency layer** that flags when the Chiefs' own play calling patterns in a given situation (down, distance, personnel, formation) have become predictable relative to league distribution — specifically, when the their play type or concept selection falls below a threshold opposing defensive coordinators could exploit.

**What is being changed:** Adding a tendency module that measures how varied the Chiefs' play selection is within specific situations, compared against league wide distributions and against the Chiefs' own historical patterns. Output would include a predictability score per situation, highlighted situations where the Chiefs have become overly tendency heavy, and recommended counter calls to restore balance.

**Why this change could improve decision making:** The core risk of any successful offense is becoming readable. Defensive coordinators invest significant film study into identifying tendencies, and even a small predictability advantage compounds across a game. Adding a self scouting layer mirrors how NFL offensive staffs already think about their own call sheets, which lowers the adoption friction. 

## Prototype Evaluation
The self scouting tendency enhancement should likely be integrated into the main project, but validation with the coaching staff is required before committing to full implementation. The main question is whether the predictability score produces useful insight. If it only confirms existing intuition, it still has value as a time saver. If it shows  missed patterns, the value is much higher.

Feedback from decision makers that would influence the integration decision includes: (1) whether the offensive coordinator finds the situations (down, distance, personnel, formation) aligned with how the staff already categorizes calls, or whether the categories need adjustment. (2) whether the predictability threshold can be calibrated to a level the staff considers meaningful rather than noisy.  (3) whether the recommended counter calls fit naturally within the existing concept library and personnel groupings, or whether they would require scheme changes the staff is unwilling to make mid season.


## Reflection on Innovation and Version Control

GitHub branches directly support the low risk experimentation by isolating the enhancement on a separate `prototype` branch, the core project on `main` stable and shareable with stakeholders while the enhancement was developed and evaluated independently. This shows how analytics teams operate in real organizations. 

GitHub also helps analytics ideas gain traction with decision makers by making the evolution of an idea visible and auditable. Commit messages document why changes were made, pull request discussions capture evaluations, and the README serves as a single source of truth that non technical staff members can read without touching any code. 

The overall workflow aligns closely with chapter 7's four phase innovation framework. The initial README commit represents the **creative phase**, by stating the idea and the decision problem it solves. The `prototype` branch represents the **prototyping phase**, by building a low cost, reversible version of an enhancement designed to demonstrate value. The evaluation section and pull request discussion represent the **engagement phase**, identifying the feedback that would influence adoption and inviting review. The final merge represents the **build phase** , which integrating the validated enhancement into the official version of the tool. 
