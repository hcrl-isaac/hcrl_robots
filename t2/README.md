# Booster T2 (31 dof, no hands)

`t2.urdf`, `t2.xml` and `meshes/` are BoosterRobotics/booster_assets @12a9751 `robots/T2/T2_31dof` (BSD-3-Clause,
`LICENSE.booster_assets`), with collision changed where Booster's leaves the body empty or simplified: a lower-trunk box
and a `waist_roll_link` box over the belly, and a sphere on each `*_shoulder_pitch_link` over the shoulder cap; in
`t2.xml` the feet collide as their meshes (convex hulls), as the URDF's do, instead of boxes. The pairs the new shapes
overlap at rest are excluded in `t2.xml` and filtered in the T2 asset cfg (`hcrl_isaaclab.assets.t2.T2_FILTERED_PAIRS`).
The URDF carries the head and waist RGB-D camera frames (`head_booster_stereo_rgb_link`,
`waist_booster_stereo_rgb_link`).

Joint ranges are Booster's published ones; they have not yet been checked against the T2's hardware stops.
