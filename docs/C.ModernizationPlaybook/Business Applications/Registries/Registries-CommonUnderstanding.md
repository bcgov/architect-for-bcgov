---
layout: default
grand_parent: Business Applications
parent: Registries
title: A Common Understanding
nav_order: 1
---

# Registries

**Archetype: Registries**

## A Common Understanding

With over 100 "registries" in the current application inventory, there appears to be a broad and varied concept of what is a registry.  At a fundamental level, a registry is where someone keeps track of things.  From the application inventory, it appears that "the thing" can be any of:
- training courses, 
- people and their contact information, 
- "people who have registered" for a program or service, 
- an event associated with a person (a birth, or a marriage, for example),
- a will,
- a person with a unique privilege, like a lobbyist,
- a person with a hunting license,
- a business and information about that business,
- information about protected areas in B.C.,
- a bridge,
- early childhood educators,
- a piece of land and its boundaries,
- title to a particular piece of land,
- public entities that trade carbon credits,
- and more.

Efforts are underway in the OCIO to recognize a set of very import things that the B.C. Government keeps track of, and to treat those things in special ways.  Most of the items in the above list will fit into this set somewhere.  That set of very important things currently looks like this:
- People
- Businesses
- Entitlements (currently under consideration, examples of this would be the permissions required to do something like fish a waterway, operate a business, or teach in the province)
- Land Parcels
- Land Titles (which arguably, could be a type of entitlement)
- Place Names
- Roads

These might be considered Master Data sets of the highest order.  There are other important data sets that we must treat in special ways, but these are considered the critical ones.  If we get information about any of these things wrong, then we're not doing good government, let alone digital government. 

The nature of a registry embodies qualities of authority, reliability, unquestionable integrity, consistency, and timeliness.  Each registry holds raw - not derived - data that is the unequivocal source.  And there is exactly one registry of record for each kind of data.  Where data in a registry must be duplicated, the registry of record remains the master.  Changes are always made to the master via a single procedure (an API, for example).  Those changes can then be propogated downstream.  With proper access to its data facilitated by the registry itself, it should be rare though, for a registry to require duplication.

As an example, government needs to keep track of information about people.  There should be one place to go - the People Registry - to get or update information about people, about a person.  There should be only one place considered the Registry of Record, which holds the definitive, authoritative, current information about a person.  No other list, spreadsheet, database, or extract, can be considered definitive. So access to the Registry of Record must be made easy for all other systems that require information about people.  Other systems that refer to a person in the People Registry will use not a person's name, but a key, a pointer (that is not an existing personal identifier like a PHN or a PEN), which provides an abstraction, and thus a tiny further element of protection.

The B.C. Government work on Data Registers has borrowed from the excellent work of the UK Government, and offers the following characteristics of a registry (subject to refinement): 
- there is a single register for each subject
- only data relevant to the subject is stored in it
- a registry contains only raw data, and nothing that is derived
- a registry uses common standard names to refer to its data
- a registry is always kept up to date by systems, not humans
- appropriate governance and ownership are in place for each 
- data in a registry is reliably the most current
- each one is declared open, shared, or private
- each is the authoritative source
- history is maintained for each record
- a record can never be lost or removed - history is maintained
- each has a named owner
- the existence 
