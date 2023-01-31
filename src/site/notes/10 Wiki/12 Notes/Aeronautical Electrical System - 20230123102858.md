---
{"dg-publish":true,"permalink":"/10-wiki/12-notes/aeronautical-electrical-system-20230123102858/"}
---

# Aeronautical Electrical System
---
The aeronautical electrical system works mainly with a [[10 Wiki/12 Notes/Battery - 20230129064209\|Battery - 20230129064209]] and an [[10 Wiki/12 Notes/Alternator - 20230126105047\|Alternator - 20230126105047]]. They're both switched on in normal operation.

A [[Regulator\|Regulator]] allows the alternator to provide exactly the power required by the servos.

> Why is the [[10 Wiki/12 Notes/Ammeter - 20230126110013\|Ammeter - 20230126110013]] positive when starting?

After starting, the ammeter is positive because the battery has been discharged and must be recharged by the alternator.


## Composition
- **Servitudes**: Power consumers (lights, radio, etc..) supplied in series or parallel.
- **[[10 Wiki/12 Notes/Alternator - 20230126105047\|Alternator - 20230126105047]]**
- [[10 Wiki/12 Notes/Battery - 20230129064209\|Battery - 20230129064209]]
- **Battery switch**
- **[[10 Wiki/12 Notes/Alternator - 20230126105047\|Alternator - 20230126105047]] switch**
- **Park switch**
- **Protections**
- **[[10 Wiki/12 Notes/Ammeter - 20230126110013\|Ammeter - 20230126110013]]**
- **[[Voltmeter\|Voltmeter]]**


## Faults

### Easement failure
In the event of a malfunction, the **C.A.P.S** procedure is used:
- **C** : Is the **Command** of the easement ON?
- **A** : **Power**: Battery ON?
- **P** : **Protection**: Fuse on or circuit breaker pushed in?
- **S**: Use of **Emergency** circuit?

In case of blown circuit breaker or fuse :
- Switch off the services supplied by the fuse.
- Change the fuse or reset the circuit breaker.
- Turn on the services one by one and identify if one of them is a problem, in this case turn it off for the rest of the flight.
- Reset the circuit breaker.
- Never force a protection**: only reset a circuit breaker once or replace a fuse once.

### Under load
Negative current => Check fuse or circuit breaker ALT fuse.

### Overloaded
Positive current => Regulator problem: switch off the alternator.

### Alternator out of order
Relieve the electrical load by reducing the number of services used.

### [[Static Electricity\|Static Electricity]]
Beware of static electricity which may cause abnormal operation of the utilities.

The aircraft is equipped with a number of electrostatic dissipators to get rid of this electricity.


## Faulty treated
Once a fault has been dealt with, the **B.A.D.** sequence is carried out:
- **Balance** : List of failed utilities.
- **Analysis**: Consequences on the flight.
- **Decision**: Continuation or interruption of the flight.





###### META
Status:: #wiki/notes/mature 
Plantations:: [[Aerotechnics\|Aerotechnics]]
References:: [[10 Wiki/14 References/Goodreads/Le Manuel de Pilotage d'Avion - 20230122071907\|Le Manuel de Pilotage d'Avion]]
