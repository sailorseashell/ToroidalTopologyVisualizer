# ToroidalTopologyVisualizer
This is a javascript application to visualize a toroidal geometry and mess with the topology by twisting, etc.

Current visualizer features

Line-only torus
The toroidal shape is drawn entirely with animated dashed lines—no surface mesh—for a clean, lightweight look.

Live geometry controls (via dat.GUI)
Hole Radius (R), Tube Radius (r), Height scale (h), Twist factor, Ripple amplitude & frequency, Line count—all rebuild the geometry instantly.

Energy-flow animation
Dash patterns slide along every line; Energy Speed slider ranges from frozen (0) to fast (0.05).

Auto-orbit
The whole structure rotates around Y; Orbit Speed slider lets you slow it to a stand-still or speed it up.

Human reference model
A low-poly CesiumMan GLB is loaded, centered inside the torus, and can be toggled with Show Human.

Responsive & efficient
• Re-creates line geometry on demand and disposes old buffers to avoid leaks.
• Reuses typed arrays to cut per-frame allocations.
• Debounced resize handler lowers reflow load.

Together these give a real-time, tweakable “cruller” torus with flowing energy lines and an optional human scale reference.