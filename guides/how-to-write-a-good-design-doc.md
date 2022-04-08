# How to Write a Good Design Doc

[Original version (made by Mothblocks)](https://hackmd.io/@tgstation/BkzmU9EyK)

Design docs are crucially important for any large feature, and beneficial even for smaller ones. It's important to know not just what you're adding, but *why*. As maintainers, we'll know better how your ideas will improve the game, as well as being able to help iron out your design. This will also help future developers not to add/remove content that doesn't align with the principles of your feature, as otherwise they'd just have to guess.

## Write your Design Docs First

Trying to write a design doc after already building the feature is like trying to make the blueprints for a house that's already built. It won't be *useless*, but if you write your design doc first, not only will it help us to clean up your design before you start making it, but it'll help *you* significantly. Writing out your ideas is a great first step to realizing their problems.

## General Writing

- Design docs should be extremely clear to read. Bullet points help a lot.
- Design docs should generally be written in present tense. Saying "medical pouches make it easier to store medical supplies" is more preferable to "medical pouches *will* make it easier to store medical supplies". This is because it *will* be the present if your PR is merged.
- Design docs *should not* include implementation details. Design docs are written for designers. Implementation details are not relevant to design (unless they are restrictive), and so should either not be included or be in their own doc.

## Important Sections

Note that while none of these are required, you should include them if you know how to fill them in. They make learning the "why" clearer for readers.

## Abstract

An abstract is a short blurb, about a paragraph or two, succinctly describing your feature. This should mostly be "why", but can include "what".

### Example
Squad specialists are a feature that allow players to occasionally become a specialised, powerful and deadly threat to the opposing force. They are picked at the start of a round and have their own unique skillset to prevent other players from being able to use the specialised gear that they are given. This means that players who join up as this role have a unique and interesting arsenal to use as opposed to every other player. However, their equipment has to be unique and noticeable, making the player more likely to be a target for xenomorphs looking to kill them.

## Goals

This is a numbered list clearly detailing your goals for the feature. As per usual, this should be a mixture of both why and what.

### Example
1. Adds a new player role that specialises in different unique and powerful weaponary. The role is handed out in a fair manner.
2. Give commanders a tool to be used in strategy and combat
3. Introduce a threat to xenomorphs that they have to deal with.

## Non-goals

Just like goals, but the opposite! Every feature has boundaries it won't step over. These should be written as if they start with "We will not...".

### Example
1. Allow the unique and powerful weaponary to be used by anyone. Xenomorphs should have a clear target to go for if they want to disable a specialist from the playing field. To do this, skills are required to use the unique specialist weapons.
2. Allow the player to completely dominate the battlefield with little to no help. Specialists should depend on their teammates to effectively push on a battlefield and remain a vulnerable target when pushing alone.

## Content

Now's where you get into clear detail about everything your feature does. **You should still be explaining 'why' things are that way, *as* you describe what.** Be as detailed as possible.

## Alternatives

Provide potential alternatives to your feature, either ones that align with your design values, or ones that don't that you suspect will be suggested. If you are including the latter, make sure to explain why you didn't choose that.

### Example

- Having the commander of each operation hand out specialist kits to players. This would make the specialist role a lot less fair as it would be handed out based on player experience, meaning that new players would not be able to try out this role. This would go against goal #1 as it wouldn't be fair to less known players who may not be as recognised as other players who often play specialist.

## Potential Changes

Most of the time you're not going to get the best design first try. It helps to try your best to predict what *could* go wrong, and suggest alternatives that can be taken, without sacrificing your design.

### Example

If it is found that specialists are disguising themselves as regular squad marines, this could defeat non-goal #1 as the unique gear on the specialist makes them obvious to xenomorphs. 

This can be adjusted by making specialists more obvious to xenomorphs, such as a HUD element being applied to each specialist.

Giving better benefits to using specialist gear could also help resolve this as specialists would be less likely to ditch their gear. This has the problem of powercreep as it could defeat non-goal #2 as the specialist may get to a point where they are able to solo the battlefield.
