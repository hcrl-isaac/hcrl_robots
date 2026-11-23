# Booster T2 (31 dof, no hands)

`t2.urdf`, `t2.xml` and `meshes/` are BoosterRobotics/booster_assets @12a9751 `robots/T2/T2_31dof` (BSD-3-Clause,
`LICENSE.booster_assets`). `t2.urdf` adds three collision shapes where Booster's leave the body empty: a lower-trunk
box and a `waist_roll_link` box over the belly, and a sphere on each `*_shoulder_pitch_link` over the shoulder cap. The
T2 asset cfg filters the pairs these overlap at rest (`hcrl_isaaclab.assets.t2.T2_FILTERED_PAIRS`). The URDF carries the head and waist RGB-D camera frames
(`head_booster_stereo_rgb_link`, `waist_booster_stereo_rgb_link`).

Joint ranges are Booster's published ones; they have not yet been checked against the T2's hardware stops.
