Life is straight forwards if you can only work with the computer interface. 

Things to think about that aren't obvious:
* Environmental factors
Size of a power connector has to be bigger for bigger wire,
should connectors protrude or stay in place (housing)

We'll mainly deal with pin headers, screw terminals, and BNC.

Types of connectors:
* Wire to wire (pins and sockets that snap together)
* board to board (press fit, copper fingers on the side of a board)
* wire to board (through hole pins that you connect to)
* power 
* modular
* terminal blocks (screw terminals that you can screw into)

Searching for connectors is a pain - digikey gets a million hits.

## Pin headers
usually 0.100'' (pitch) rectangular pins. DON'T ACCIDENTALLY GET THE WRONG SPECIALTY THING

DON'T USE FOR BOARD TO BOARD CONNECTIONS. Sticking together and pulling apart has a lot of friction - usually better to have a ribbon. Separate mechanical and electrical connection. 

On digikey: Search for conn hdr or conn header, select Headers, male pins (not the specialty option!).

If you want mechanical support, look for locks. If you have a ribbon cable receptacle, there are usually flaps on the side that snap up. Similar ideas, zero insertion force sockets.

Shrowds: If you have a series of pins that have a piece of plastic, the plastic shell is the "shrowd". Makes mechanically handling easier. The shrowd can be "keyed", which means that the shrowd has a plastic protrusion/hole - this way, its impossible to have connections in the wrong orientation. 



## Insulation Displacement Contact Connectors
when you install these on a ribbon cable, they punch through the insulation to make contact with the metal wire.

Ribbon cables have a few issues: there can be a lot of coupling between the wires (its a single ended connection) and is susceptible to electromagnetic waves and parastic behavior. This can be avoided by putting ground lines between important wires.

Find the IDC mounts under: free hanging panel mount in digikey.
![[OIP-320812468.jpeg]]


## Japan Solderless Terminal (JST) connectors

![[OIP-3275142685.jpeg]]

## DIN Connectors
These are common for audio cables.
Make sure you don't get a PS2 cable.
![[OIP-3955568388.jpeg]]
## D-Sub Connectors
Old serial connections. 
Used for hermetic sealing (acid/water proof).
![[OIP-2946492329.jpeg]]

## Board-to-board Connectors
Select "Edge plating" so that they are thick enough. You can get great signal density, its cheap, common connection. 
![[OIP-4209174717.jpeg]]

## DuPont Connectors
Not an actual connector, but colloquially called this. Its the 
![[OIP-3720544718.jpeg]]

## Molex Connector
usually for power delivery
tight locking connection
![[OIP-3207411693.jpeg]]

## IEC Cable
![[OIP-3613855477 1.jpeg]]
