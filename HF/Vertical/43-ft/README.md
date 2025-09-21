# 43 Foot Vertical
43 ft verticals were or are quite popular. Usually ground mounted, with an ATU at the base ideally.

On 20m band they are a 5/8, above 20m they radiate more at higher angles with less gain at lower angles where it's preferred. 60m band they approx. 1/4 wave, on 80m they're a bit short with a low impedance, but will work with a good ATU. 

Some mfgrs recommend 4:1 unun and ~150 ft of coax, then a shack ATU. Great if you like heating up coax I suppose.. Anytime long lengths of coax are recommended is usually a very bad sign. To know how much power will be lost in the coax, use [TL Details](https://ac6la.com/tldetails1.html), input the source impedance (Src Data) from the model (In TL Details, Impedance = R, J = X), enter length of coax etc, and see what the results are.

Ground mounted: At a minimum a 1:1 current balun should sit between the vertical + ground (buried radials) and a remote ATU at the feed-point to force equal and opposite currents into the antenna system, the coax and control cable shields should also have current chokes on them where they exit the ATU.

Elevated: The radials should be electrically isolated from any metallic masts the antenna is attached to, otherwise the mast will become part of the the antenna system and act like vertical dipole. A 1:1 current balun should sit between the feed-point and a remote ATU, or via open wire line (450 or 600 Ω) to an ATU with another 1:1 current balun - I'm not 100% sure you need to have 1:1 baluns at each end of the balanced line, or just the ATU end. Either way the balun forces equal and opposite currents to flow into the antenna system, and prevents the feed-line from becoming part of the antenna system and radiating (causing RFI/noise pickup).

The models are slightly shorter at 40 ft or 12.2m, and use 12 AWG copper wire. Suit using 40 ft Spider-beam pole. 

## 43 Ft Elevated

43ft-Vertical-Elev.ez

Elevated with 40 ft radials. At 20m higher angle lobe is starting to become dominate, due to the radials being too long. If shortened impedance on 80m starts getting too low for reasonable ATU efficiency.

## 43 Ft Elevated With 50 Ω Match

43ft-Vertical-Elev-40m.ez

Using shorter radials 5.75m, we get a 50 Ω match < 1.5:1 from 7.0 to 7.2 MHz. Isolating the radials from any metallic mast, and using a 1:1 current balun is a must since the antenna system is un-balanced - it will want to work against the mast or coax shield if they're not isolated.

## 43 Ft Ground Mounted

43ft-Vertical-GndMtd.ez