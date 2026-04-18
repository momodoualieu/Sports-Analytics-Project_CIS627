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
