# Summary

Once a space reaches a membership of more than around ten people, it
becomes impractical to maintain access via keys and duplication. The cost
is prohibitive and the security it provides decreases with each and every
duplicate set you have cut.

Access control enables your members to gain access to your space without
the need for a set of keys and enables revocation of expired members
access without the need to get keys back from that member.

Don't get carried away with your security concerns on the electronics and
network side when considering physical access control.

Locks of any kind will only protect you against honest people, most things
don't stand up well when hit with a large hammer or a determined
individual.

Core components:

* Access tokens
* Readers
* Ironmongery
* Controller

# Access Tokens

Cards or tokens for access can come in many different types of technology,
we'll cover a few here for reference.

## Magnetic stripe

Whilst mostly obsolete, magnetic track card readers are still fairly
common in many places with all UK bank cards still having this facility.

Unless you manage to obtain a low cost or free supply of readers and
cards, it's not worth investing in this technology at this point.

If you do choose this technology you will need to program your own cards
as using bank cards will reveal morew information to the reader than you
want to see. Limit your card numbers to 12 digits if you hope to have
any compatibility with commercial off the shelf solutions.

Due to the contact based nature, the card and reader will wear out and
require replacement.

Despite all of this, they are still commonly found in hotels worldwide.

See also:

* https://en.wikipedia.org/wiki/Magnetic_stripe_card
* https://en.wikipedia.org/wiki/Wiegand_interface

## Contactless Tokens

Contactless tokens generally come in two frequencies:

* 125KHz
* 13.56MHz

See also https://en.wikipedia.org/wiki/Radio-frequency_identification

Most contactless tokens are available in multiple formats such as cards,
keyfobs or even stickers.

The main difference between the two main frequency standards is that of
range and amount of data.

The 125KHz tokens are generally longer range but only transmit a serial
number.

The 13.56MHz tokens are much shorter range (typically 10cm or less) but can
perform much more complex operations including levels of encryption and
security beyond those available at the lower frequency.

### MiFare 

MiFare is one of the defacto 13.56MHz contactless smart token standards and
is widely adopted. You may be familiar with it in one of the following:

* Oyster card
* Contactless bank payment cards
* University library or ID cards



See also https://en.wikipedia.org/wiki/MIFARE



## Other technologies

The following technologies are also available but were not discussed:

* Contact based smart cards
* Barcode or QR code

Generally these would not be considered suitable for controlling access.

# Readers

## General recommendations


## Recommended Readers


# Ironmongery

There are as many locking options as there are types of door for them to
installed upon, so whilst it's possible to give general advice every door
and circumstance is different.

When looking at locking hardware, the first piece of information one must
consider is the mode in which they fail.

## Fail Open (FO)

Fail Open or Fail Safe locks as implied fail in a manner that leaves the
door insecure. This type of lock should not be used on an external door
unless suitable battery backup is provided to retain security in the event
of a power outage.

The lock is released by interrupting power supplied to the lock. A Break
Glass Unit must be installed to permit the door to open regardless of the
status of the controller. It is adviseable to monitor actuation of the
Break Glass Unit to prevent it being activated and the door being left in
an insecure state for an unknown period of time.

Consideration should also be given to if the door should open on sounding
of a fire alarm. Whilst it may seem obvious that doors on the path of a
fire escape route should automatically open on sounding, there are
occasions when this is not entirely clear and advice should be sought from
your local fire service. Consultation with the fire services college does
not guarantee compliance with your local fire service. If in doubt,
consult with your local fire service before performing installation work.

As an external door would likely be a fire exit, the likelihood of the
fire service requiring it to fail open when the fire alarm is sounding is
another reason to consider this an unsuitable locking mechanism for an
external door.

## Fail Secure (FS)

Fail secure locks result in the door being left in a secure, closed state.

The lock is released by applying power to the locking mechanism. This type
of lock is normally an electronic enablement to a traditional locking
mechanism such as an electronic strike plate.

Due to the way in which this is a mechanical enablement to a traditional
locking mechanism, there are fewer considerations to interconnection with
fire alarms though as with fail open locks, it is wise to consult your
local fire service should you be in any doubt of the safety requirements.

Fail secure locks are recommended.

## Recommended Locking Hardware

Whilst many locking mechanisms exist, the following come recommended
depending on the specific circumstances.

### Abloy EL560

See http://tinyurl.com/z47cumu

This lock is extremely expensive and requires installation by a suitably
skilled locksmith. It is a traditional lock in all appearances but does
not work in a traditional manner.

The handles on either side of the door operate independently with an
electronic enablement.

It can be configured to operate Fail Secure or Fail Open, it can also be
configured to operate opening inwards or outwards.

### Cisa

* 11610 - http://www.saundersonsecurity.co.uk/acatalog/Cisa_11610_Rim_Electric_Locks.html 
* 1A721 - http://www.saundersonsecurity.co.uk/acatalog/Cisa_Elettrika_1A721_Elec_lock_For_Metal_1A721.html

These locks are fail secure and are released by application of 24v AC.

Whilst the Cisa locks offer a great value and level of security they are
very specifically handed and direction focused. You need to know which
direction your door opens (inwards or outwards) and if it is hinged on the
left or right. See this handy diagram:

```
  +--------+   +--------+
  | 1      |   | 2      |
  |    \   |   |   /    |
  +---  ---+   +---  ---+

  +--------+   +--------+
  | 3      |   | 4      |
  |        |   |        |
  +---  ---+   +---  ---+
       /           \
```

* 1. Right hand inward opening
* 2. Left hand inward opening
* 3. Right hand outward opening
* 4. Left hand outward opening

Make sure that you purchase the correct handing and direction when
ordering as it cannot be changed.

This is the lock of choice for London and Manchester Hackspaces.

### Effeff Electric Strike

Available in fail open or fail secure flavours and for different
voltages.

One of the main considerations when using this type of release is the lock
that it is paired with.

Suggested lock: Imperial Locks G7088

This is an oval cylinder lock and may not be suitable for your
circumstances. The main considerations should be:

Provision of an override lock should the system fail.

It should have an anti thrust bolt to prevent it being pushed back by
inserting something between the door and frame.  Distance between main
latch and anti thrust bolt should be checked to ensure that the anti
thrust component falls outside the gap created for the latch.

## Other considerations

### DDA


### Fire escape routes


 
