Author: Angela Vitaletti
Date: 06 February 2017
Description: This is my Unreal Project for IT-266 at NJIT.

The goal here was to make it crash, and then apply the same behvior, but prevent the crash.

In making it crash I modified the following blueprints:
FirstPersonProjectileCrash.uasset

The chaotic goal in modifying this file was to have a projectile (firecracker) spawn a 
child once it collided with something. I did that successfully and as soon as I fired,
spawning began, and the whole thing crashed in seconds.

When making it work correctly, I modified the following two blueprints:
FirstPersonProjectile.uasset
FirstPersonCharacter.uasset

In the Projectile blueprint, I have two loops. The inner loop controls the child spawning
and the loop itself limits it to one generation, but allows for a certain amount of 
children in that generation to be spawned. The outer loop controls the
inner one, making for more chaos, but also to allow multiple projectiles to spawn
multiple children.

In the Character blueprint, I implemented a delay for the firing, a "cool-down." This
also protects against lag in that the player cannot fire many times and have many, many
projectiles spawned to cause lag or a crash.

The two files with "Crash" at the end of them are the files that were used when it
crashed. The files with the same name, but without the "Crash" are used in the 
completed, functioning project.

In Unreal, I used the First Person Shooter template.