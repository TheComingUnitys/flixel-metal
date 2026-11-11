# Metal instancing support (Codename Metal fork)

Flixel itself does not issue draw calls; its sprites are Bitmaps rendered by OpenFL.  This
fork adds FlxG.metalInstancing (default true), which toggles the OpenFL-level
MetalInstanceBatch when the metal_instancing define is enabled.  No behavioural change
without that define.
