# Ergonomic Dual Foot Controller
<img width="1159" height="679" alt="1" src="https://github.com/user-attachments/assets/b061340f-652e-4ea7-b0b8-1a71fb33d658" />
<img width="1058" height="674" alt="3" src="https://github.com/user-attachments/assets/920d171a-d41f-4c15-8e72-dcb9f11a3db4" />
<img width="1280" height="516" alt="2" src="https://github.com/user-attachments/assets/6b9a65df-eadc-4eec-9b1b-cc86766881a2" />
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

I found a great reference model with the [Adafruit Three Button Foot Switch](https://learn.adafruit.com/three-button-foot-switch/overview) and based my design off it. The original design had its own issues:
- The snap-on hinges felt too flimsy and wobbly. I added long machine screws for a more stable, reliable pedal.
- The pedal design wasn’t ergonomic enough.

So now the design for this foot controller comes down to
- The best height for each pedal.
- The best switch for each pedal.
- The best operation force (OF) for each pedal.

The solution I came up with was 12x12x4.3mm tactile switches. You can find them in a variety of operating forces (130 gf to 350 gf) on Digikey. The switch has very low travel (0.3mm), very tactile and audible click, and has a high enough OF where you can rest your toes on the pedal and not activate it. You can mount the switch on 2cm wide perboard, just remember to cut off the bottom plastic pins so it can be flush with the board. 

I would recommend editing the controller’s width, height, and choosing a tactile switch by operating force to fit your needs. Print one side of the controller to test out and adjust accordingly.

As for software, it's a simple two button controller so choose any option you like: QMK/Arduino/Etc. You can even use the microcontroller and code from the [Adafuit build guide](https://learn.adafruit.com/three-button-foot-switch/overview) (though that one is USB-C, not Micro-USB). I used QMK.

The image shows how I lay my toes on the controller. I had socks on but I think it's easier to operate it without them.

I’ve used this controller for FPS games for sliding and jumping and it works great. I hope it’ll help someone else not just for gaming but for people with hand disabilities who can use it for mouse left click and right click.

## Parts List
- Two 12x12x4.3mm Tactile Switches 
  - B3F-4000 (OF: 130 gf): [link](https://www.digikey.com/en/products/detail/omron-electronics-inc-emc-div/B3F-4000/63961)
  - PTS125SM43-2 LFS (OF: 180 gf): [link](https://www.digikey.com/en/products/detail/c-k/PTS125SM43-2-LFS/1146743)
  - B3W-4000 (OF: 200 gf): [link](https://www.digikey.com/en/products/detail/omron-electronics-inc-emc-div/B3W-4000/31780)
  - B3F-4005 (OF: 260 gf): [link](https://www.digikey.com/en/products/detail/omron-electronics-inc-emc-div/B3F-4005/20679) (The one I used)
  - B3W-4005 (OF: 350 gf): [link](https://www.digikey.com/en/products/detail/omron-electronics-inc-emc-div/B3W-4005/368404)
- 2 x 8 cm perfboard: [link](https://www.amazon.com/dp/B07Y3GMWD9?ref_=ppx_hzsearch_conn_dt_b_fed_asin_title_3&th=1)
- cSeao 20-Set 304 Stainless Steel M3x80mm Phillips Pan Head Machine Screws with M3 Nuts: [link](https://www.amazon.com/gp/product/B07D4KMW47/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1)
- Micro USB Male to Micro USB Female Extension Panel Mount Type Cable with Screws, Data+Charge,Black 50CM/1.6FT: [link](https://www.amazon.com/gp/product/B07DJB7ZFV/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
- Velcro to mount the microcontroller: [link](https://www.amazon.com/VELCRO-Brand-Fasteners-Industrial-VEL-30703-USA/dp/B09BNPX3XJ?crid=22WDORFD48PX&dib=eyJ2IjoiMSJ9.6P0m0RfMJFEWBiqtTsrMbYhd2FDMmycihfXly0lk9wCfrd6YHS3PPqA4TZwgo76cMr_srcihzwctbhHLwbTkBO45XFZhQlAcXVNpt4epqf7HRENuXFcPO09pytYnZVSgq_aR5xMfiFuo0pUbaEpG8eC31tPty_lJrkjjWrUtrBfK2yBkmLKilujCSLAPztMOEknfQnD1lRRjoMrOr12XevjlQbzBhFp2Hhx-FoAN6pM.vHi_gN894NLd6jCdeLinPm37dUyH48G4GSz67TxEQGk&dib_tag=se&keywords=velcro&qid=1732865486&sprefix=velcro%2Caps%2C193&sr=8-1)
- 1mm Rubber Gasket: [link](https://www.amazon.com/gp/product/B0C9Y7DVDN/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
- uxcell knurled Insert Nuts, 60Pcs M3 x 6mm L x 5mm OD 3D Printing Brass Nuts Female Threaded Inserts Brass Heat Set Insert Embedment Nut: [link](https://www.amazon.com/gp/product/B09MCXH78P/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
- AINOPE Micro USB Cable 6.6ft USB to Micro USB Charger Cable Right Angle: [link](https://www.amazon.com/dp/B0BTH4NZ8M?ref=ppx_yo2ov_dt_b_fed_asin_title)
- Pro Micro
- Four M3-0.5 x 12mm Countersunk Flat Head Phillips Machine Screws
- Gorilla 2 Part Epoxy, Clear Epoxy: [link](https://www.amazon.com/Gorilla-Epoxy-Minute-ounce-Syringe/dp/B001Z3C3AG?th=1)
