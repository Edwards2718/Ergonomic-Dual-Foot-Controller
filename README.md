# Ergonomic Dual Foot Controller

<img width="1074" height="351" alt="Internals" src="https://github.com/user-attachments/assets/932aea83-4cef-4d4b-b426-e637dd4aabc4" />

The key features I wanted for this foot controller were ergonomics and performance. That means that I wanted a controller that would not fatigue the legs and feet throughout its use and have very responsive controls, whether for gaming or work use. I have issues with what’s available on the market since those pedals are stiff, have very large press-travel, and some you have to hover your foot to avoid activating the switch. My idea was to have something akin to having a hand, resting on a table, pressing a mouse button.

So, what I wanted in a foot controller was:
- Only exertion needed is from the big toes
- The big toes can rest on the pedals without activating them
- Legs be in a relaxed state
- Only requires downward presses from the big toes
- Does not feel awkward to use, at all
- Is not fatiguing to use
- No exertion needed from the ankles or calves
- Can easily be put away when not in use
- Low-profile

My testing concluded that, at least for me, only the big toes have enough dexterity to effectively operate pedals. I tried out multiple 4-pedal toe-controlled designs but all toes seem to move together to some degree, creating issues with accidental pedal presses.

I found a great reference model with the Adafruit Three Button Foot Switch and based my design off it, but it had its own issues:
- The snap-on hinges felt too flimsy and wobbly. I added long machine screws for a more stable, reliable pedal.
- The pedal design wasn’t ergonomic enough.

So now the design for this foot controller comes down to
- The best height for each pedal.
- The best switch for each pedal.
- The best operation force (OF) for each pedal.

The solution I came up with was 12x12x4.3mm tactile switches. You can find them in a variety of operating forces (130 gf to 350 gf) on Digikey. The switch has very low travel (0.3mm), very tactile and audible click, and has a high enough OF where you can rest your toes on the pedal and not activate it. You can mount the switch on 2cm wide perboard, just remember to cut off the bottom plastic pins so it can be flush with the board.  

As for software, it's a simple two button controller so choose any option you like: QMK/Arduino/Etc. I used QMK.

I’ve used this controller for FPS games for sliding and jumping and it works great. I hope it’ll help someone else not just for gaming but for people with hand disabilities who can use it for mouse left click and right click.

Parts List
- Two 12x12x4.3mm Tactile Switches 
  - B3F-4000 (OF: 130 gf): link
  - PTS125SM43-2 LFS (OF: 180 gf): link
  - B3W-4000 (OF: 200 gf): link
  - B3F-4005 (OF: 260 gf): link (The one I used)
  - B3W-4005 (OF: 350 gf): link
- 2 x 8 cm perfboard: link
- cSeao 20-Set 304 Stainless Steel M3x80mm Phillips Pan Head Machine Screws with M3 Nuts: link
- Micro USB Male to Micro USB Female Extension Panel Mount Type Cable with Screws, Data+Charge,Black 50CM/1.6FT: link
- Velcro to mount the microcontroller: link
- 1mm Rubber Gasket: link
- uxcell knurled Insert Nuts, 60Pcs M3 x 6mm L x 5mm OD 3D Printing Brass Nuts Female Threaded Inserts Brass Heat Set Insert Embedment Nut: link
- AINOPE Micro USB Cable 6.6ft USB to Micro USB Charger Cable Right Angle: link
- Pro Micro
- Four M3-0.5 x 12mm Countersunk Flat Head Phillips Machine Screws
- Gorilla 2 Part Epoxy, Clear Epoxy: link
