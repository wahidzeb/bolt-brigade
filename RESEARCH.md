# Bolt Brigade – Research & Design Notes

## What the genre leaders do
| Game | Core loop | Controls | Progression / economy | Bosses |
|---|---|---|---|---|
| **Cover Fire** (1MB) | Rail shooter: you stay in cover, pop out, clear a wave, auto-advance to the next spot. "Aim. Shoot. Wait." | Press to aim/pop out, release to drop back into cover (3D-touch original). | 13 episodes × 12 stages, 60+ missions; cash + skill cards upgrade cover durability, damage, reload, accuracy (combat level). Energy timers & long upgrade waits are its most-hated parts. | Platoon bosses: wait until the boss stops firing / turns, clear foot soldiers first, shoot grenades in the air. |
| **Time Crisis** (arcade) | Short timed "action scenes", hide with a pedal, reload only while hidden, red-flash "danger" shots telegraph hits you must dodge. | One trigger + one hide pedal: the two-button purity is why it's fun. | Linear stages, score/time; the timer pushes you to pop out. | Multi-phase set-piece bosses with clear weak points and readable attack tells. |
| **Gun Strike / Sniper-style mobile shooters** | 30–90 s missions, 3–5 waves, then results + coins. | Hold-to-aim, auto-fire on target, swipe to look. | Weapon shop: many guns, 4-ish upgrade stats each, stars per level, daily login rewards. | Vehicles (tanks, helicopters) with rockets you can shoot down. |
| **Web .io cover shooters** (e.g. top-down arena games) | Instant play, sessions under 2 minutes. | One-thumb, auto-fire when a target is in range is the norm on mobile. | Cosmetics/levels, very light. | Rare. |

## What makes it fun (takeaways)
1. **The peek rhythm is everything**: risk (exposed, dealing damage) vs safety (hidden, reloading). Enemy shots must be **telegraphed** (charge glow, laser lines, visible slow bolts) so hiding is a skill, not luck.
2. **One-thumb control**: hold = pop out + auto-fire, drag = aim (with aim assist), release = hide + reload. No separate fire button.
3. **Destructible cover both ways**: shoot crates apart to expose enemies; rockets/grenades chip *your* cover, so you can't hide forever.
4. **Short levels (45–120 s), 3–5 waves**, results screen with stars and coins, then an upgrade to buy: a tight dopamine loop.
5. **Enemy variety creates decisions**: shooters, shield-bearers, grenade lobbers (shoot grenades mid-air), snipers (laser tell), rushers (must be shot before they reach you), drones, heavies with rockets.
6. **Bosses with weak points + phases**, minions, and attacks you dodge by hiding.
7. Avoid the genre's pain points: **no energy, no waiting timers, no paywalls**.

## Bolt Brigade design (original)
- **Theme**: wind-up toy robots vs. the player's toy brigade. Hits make sparks, bolts and springs; defeated robots pop apart and fizzle. No blood, no humans harmed.
- **Controls**: hold anywhere = pop out & auto-fire at the reticle (aim assist snaps to targets, Strong/Light/Off). Drag while holding to aim. Release = hide; magazine reloads while hidden. Desktop: mouse/space. EMP special button charges from damage dealt.
- **Enemies**: Clank (grunt), Shieldy (shield, breakable), Lobber (grenades, shootable), Zipper (drone), Spotter (sniper, laser tell), Roller (rusher), Brute (heavy, rockets that chip cover). Explosive barrels chain-react.
- **Content**: 5 stages × 7 levels = 35 levels (Toy Yard, Dune Depot, Frost Fort, Neon Works, Sky Citadel); level 7 of each stage is a multi-phase boss with glowing weak points.
- **Economy**: coins from kills/clears; 5 weapons (Pea Blaster, Buzz SMG, Scatter Popper, Zap Rail, Boom Tube) each with Damage/Rate/Mag/Reload upgrades; gear upgrades Armor, Cover, EMP. Stars: clear / ≥50% HP / ≥85% HP. Daily reward 7-day streak. Saves merged with defaults and validated.
- **Tech**: Canvas 2D pseudo-3D (perspective depth, pre-rendered shaded sprites, additive lighting, particles, screen shake), adaptive quality (DPR + particle caps by measured frame time), WebAudio synth SFX + music.
