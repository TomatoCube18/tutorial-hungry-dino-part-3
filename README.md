### @explicitHints true
 
# tutorial



## Step 1
**v1.0: This guide is created to assist you throughout the live stream. **

**Step 1**
1. Click on the **Advanced** arrow to expand more category
2. Open the ``||scene.Functions||`` drawer, click on **Make a Function...**
3. Rename **doSomething** to **create_map** 
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_2.png)



### ~ tutorialhint
```blocks
function create_map () {
}

```

```ghost

let projectile: Sprite = null
projectile.lifespan = 3000
    if (projectile.isHittingTile(CollisionDirection.Bottom)) {
        projectile.vy = -135
    }
projectile.setImage(img`
        . . . . . . . . . . . . . . . . 
        . . f f f f f f f f . . . . . . 
        . f 7 7 7 7 7 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f f . . . . 
        . f 7 7 1 1 1 7 7 7 f 4 . . . . 
        . f 7 7 7 7 7 f 7 7 f 4 4 . . . 
        . . f f f f f f 7 7 7 f f . . . 
        . . . . f 7 7 7 7 7 7 f 4 . . . 
        . . f 7 7 7 7 7 7 f 7 f 4 4 . . 
        . . f 7 7 7 7 7 7 f 7 7 f f . . 
        . . . . f 7 d d 7 7 7 7 f 4 4 . 
        . . . . f 7 d d d 7 7 7 7 f f 4 
        . . . . f 7 d d d 7 7 7 7 7 7 f 
        . . . . f 7 d f f 7 7 f f f f f 
        . . . . f f f . . f f f . . . . 
        `)

scene.placeOnRandomTile(projectile, 9)      
scene.cameraFollowSprite(projectile)

controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (projectile.isHittingTile(CollisionDirection.Bottom)) {
        projectile.vy = -140
    }
})  
``` 


```template
enum ActionKind {
    walking_right,
    walking_left
    standing_right,
    standing_left
}
namespace SpriteKind {
    export const background = SpriteKind.create()
}
function create_walking_animation () {
    anim_walk_left = animation.createAnimation(ActionKind.walking_left, 100)
    anim_walk_left.addAnimationFrame(img`
        . . . . . . . . . . . . . . . . 
        . . f f f f f f f f . . . . . . 
        . f 7 7 7 7 7 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f f . . . . 
        . f 7 7 1 1 1 7 7 7 f 4 . . . . 
        . f 7 7 7 7 7 f 7 7 f 4 4 . . . 
        . . f f f f f f 7 7 7 f f . . . 
        . . . . f 7 7 7 7 7 7 f 4 . . . 
        . . . . f 7 7 7 7 7 7 f 4 4 . . 
        . . . . f 7 7 7 7 7 7 7 f f . . 
        . . . . f 7 d d f 7 7 7 f 4 4 . 
        . . . . f 7 d f 7 7 7 7 7 f f 4 
        . . . . f 7 f 7 7 7 f 7 7 7 7 f 
        . . . . f f f 7 7 f f f f f f f 
        . . . . . . . f f f . . . . . . 
        `)
    anim_walk_left.addAnimationFrame(img`
        . . . . . . . . . . . . . . . . 
        . . f f f f f f f f . . . . . . 
        . f 7 7 7 7 7 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f f . . . . 
        . f 7 7 1 1 1 7 7 7 f 4 . . . . 
        . f 7 7 7 7 7 f 7 7 f 4 4 . . . 
        . . f f f f f f 7 7 7 f f . . . 
        . . . . f 7 7 7 7 7 7 f 4 . . . 
        . . . . f 7 7 7 7 7 7 f 4 4 . . 
        . . . . f 7 7 7 7 7 7 7 f f . . 
        . . . . f 7 7 f 7 7 7 7 f 4 4 . 
        . . . . f 7 7 f 7 7 7 7 7 f f 4 
        . . . . f 7 7 d f 7 7 7 7 7 7 f 
        . . . . f 7 7 d f 7 7 f f f f f 
        . . . . f f f . . f f f . . . . 
        `)
    anim_walk_left.addAnimationFrame(img`
        . . . . . . . . . . . . . . . . 
        . . f f f f f f f f . . . . . . 
        . f 7 7 7 7 7 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f f . . . . 
        . f 7 7 1 1 1 7 7 7 f 4 . . . . 
        . f 7 7 7 7 7 f 7 7 f 4 4 . . . 
        . . f f f f f f 7 7 7 f f . . . 
        . . . . f 7 7 7 7 7 7 f 4 . . . 
        . . . . f 7 7 7 7 7 7 f 4 4 . . 
        . . . . f 7 7 7 7 7 7 7 f f . . 
        . . . f f 7 d d d 7 7 7 f 4 4 . 
        . . . f 7 7 d d 7 7 7 7 7 f f 4 
        . . . f 7 7 d d 7 7 7 7 7 7 7 f 
        . . . f f f f f f 7 7 f f f f f 
        . . . . . . . . . f f f . . . . 
        `)
    anim_walk_left.addAnimationFrame(img`
        . . . . . . . . . . . . . . . . 
        . . f f f f f f f f . . . . . . 
        . f 7 7 7 7 7 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f f . . . . 
        . f 7 7 1 1 1 7 7 7 f 4 . . . . 
        . f 7 7 7 7 7 f 7 7 f 4 4 . . . 
        . . f f f f f f 7 7 7 f f . . . 
        . . . . f 7 7 7 7 7 7 f 4 . . . 
        . . f 7 7 7 7 7 7 f 7 f 4 4 . . 
        . . f 7 7 7 7 7 7 f 7 7 f f . . 
        . . . . f 7 d d 7 7 7 7 f 4 4 . 
        . . . . f 7 d d d 7 7 7 7 f f 4 
        . . . . f 7 d d d 7 7 7 7 7 7 f 
        . . . . f 7 d f f 7 7 f f f f f 
        . . . . f f f . . f f f . . . . 
        `)
    anim_walk_right = animation.createAnimation(ActionKind.walking_right, 100)
    anim_walk_right.addAnimationFrame(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . f f f f f f f f . . 
        . . . . 4 f 7 7 7 7 7 7 7 7 f . 
        . . . . 4 f 7 7 7 1 f 1 7 7 f . 
        . . . . f f 7 7 7 1 f 1 7 7 f . 
        . . . . 4 f 7 7 7 1 1 1 7 7 f . 
        . . . 4 4 f 7 7 f 7 7 7 7 7 f . 
        . . . f f 7 7 7 f f f f f f . . 
        . . . 4 f 7 7 7 7 7 7 f . . . . 
        . . 4 4 f 7 7 7 7 7 7 f . . . . 
        . . f f 7 7 7 7 7 7 7 f . . . . 
        . 4 4 f 7 7 7 f d d 7 f . . . . 
        4 f f 7 7 7 7 7 f d 7 f . . . . 
        f 7 7 7 7 f 7 7 7 f 7 f . . . . 
        f f f f f f f 7 7 f f f . . . . 
        . . . . . . f f f f . . . . . . 
        `)
    anim_walk_right.addAnimationFrame(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . f f f f f f f f . . 
        . . . . 4 f 7 7 7 7 7 7 7 7 f . 
        . . . . 4 f 7 7 7 1 f 1 7 7 f . 
        . . . . f f 7 7 7 1 f 1 7 7 f . 
        . . . . 4 f 7 7 7 1 1 1 7 7 f . 
        . . . 4 4 f 7 7 f 7 7 7 7 7 f . 
        . . . f f 7 7 7 f f f f f f . . 
        . . . 4 f 7 7 7 7 7 7 f . . . . 
        . . 4 4 f 7 7 7 7 7 7 f . . . . 
        . . f f 7 7 7 7 7 7 7 f . . . . 
        . 4 4 f 7 7 7 7 f 7 7 f . . . . 
        4 f f 7 7 7 7 7 f 7 7 f . . . . 
        f 7 7 7 7 7 7 f d 7 7 f . . . . 
        f f f f f 7 7 f d 7 7 f . . . . 
        . . . . f f f . . f f f . . . . 
        `)
    anim_walk_right.addAnimationFrame(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . f f f f f f f f . . 
        . . . . 4 f 7 7 7 7 7 7 7 7 f . 
        . . . . 4 f 7 7 7 1 f 1 7 7 f . 
        . . . . f f 7 7 7 1 f 1 7 7 f . 
        . . . . 4 f 7 7 7 1 1 1 7 7 f . 
        . . . 4 4 f 7 7 f 7 7 7 7 7 f . 
        . . . f f 7 7 7 f f f f f f . . 
        . . . 4 f 7 7 7 7 7 7 f . . . . 
        . . 4 4 f 7 7 7 7 7 7 f . . . . 
        . . f f 7 7 7 7 7 7 7 f . . . . 
        . 4 4 f 7 7 7 d d d 7 f f . . . 
        4 f f 7 7 7 7 7 d d 7 7 f . . . 
        f 7 7 7 7 7 7 7 d d 7 7 f . . . 
        f f f f f f 7 7 f f f f f . . . 
        . . . . . f f f . . . . . . . . 
        `)
    anim_walk_right.addAnimationFrame(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . f f f f f f f f . . 
        . . . . 4 f 7 7 7 7 7 7 7 7 f . 
        . . . . 4 f 7 7 7 1 f 1 7 7 f . 
        . . . . f f 7 7 7 1 f 1 7 7 f . 
        . . . . 4 f 7 7 7 1 1 1 7 7 f . 
        . . . 4 4 f 7 7 f 7 7 7 7 7 f . 
        . . . f f 7 7 7 f f f f f f . . 
        . . . 4 f 7 7 7 7 7 7 f . . . . 
        . . 4 4 f 7 f 7 7 7 7 7 7 f . . 
        . . f f 7 7 f 7 7 7 7 7 7 f . . 
        . 4 4 f 7 7 7 7 d d 7 f . . . . 
        4 f f 7 7 7 7 d d d 7 f . . . . 
        f 7 7 7 7 7 7 d d d 7 f . . . . 
        f f f f f 7 7 f f d 7 f . . . . 
        . . . . f f f . . f f f . . . . 
        `)
    animation.attachAnimation(dino, anim_walk_left)
    animation.attachAnimation(dino, anim_walk_right)
}
function create_dino () {
    dino = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . f f f f f f f f . . 
        . . . . 4 f 7 7 7 7 7 7 7 7 f . 
        . . . . 4 f 7 7 7 1 f 1 7 7 f . 
        . . . . f f 7 7 7 1 f 1 7 7 f . 
        . . . . 4 f 7 7 7 1 1 1 7 7 f . 
        . . . 4 4 f 7 7 f 7 7 7 7 7 f . 
        . . . f f 7 7 7 f f f f f f . . 
        . . . 4 f 7 7 7 7 7 7 f . . . . 
        . . 4 4 f 7 f 7 7 7 7 7 7 f . . 
        . . f f 7 7 f 7 7 7 7 7 7 f . . 
        . 4 4 f 7 7 7 7 d d 7 f . . . . 
        4 f f 7 7 7 7 d d d 7 f . . . . 
        f 7 7 7 7 7 7 d d d 7 f . . . . 
        f f f f f 7 7 f f d 7 f . . . . 
        . . . . f f f . . f f f . . . . 
        `, SpriteKind.Player)
    controller.moveSprite(dino, 50, 0)
    dino.ay = 290
    scene.cameraFollowSprite(dino)
    scene.placeOnRandomTile(dino, 9)
    create_stand_animation()
    create_walking_animation()
}
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (dino.isHittingTile(CollisionDirection.Bottom)) {
        dino.vy = -140
    }
})
controller.left.onEvent(ControllerButtonEvent.Pressed, function () {
    animation.setAction(dino, ActionKind.walking_left)
})
scene.onHitTile(SpriteKind.Player, 10, function (sprite) {
    game.over(true)
})
controller.right.onEvent(ControllerButtonEvent.Released, function () {
    animation.setAction(dino, ActionKind.standing_right)
})
controller.left.onEvent(ControllerButtonEvent.Released, function () {
    animation.setAction(dino, ActionKind.standing_left)
})
controller.right.onEvent(ControllerButtonEvent.Pressed, function () {
    animation.setAction(dino, ActionKind.walking_right)
})
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    otherSprite.destroy()
    music.jumpUp.play()
})
function create_eggs () {
    tile_list = scene.getTilesByType(5)
    for (let value of tile_list) {
        egg = sprites.create(img`
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . f f . . . . . . . 
            . . . . . . f 5 5 f . . . . . . 
            . . . . . f 5 5 5 5 f . . . . . 
            . . . . . f 5 1 1 5 f . . . . . 
            . . . . f 5 5 5 1 5 5 f . . . . 
            . . . . f 5 5 5 5 5 5 f . . . . 
            . . . . f 5 5 5 5 5 5 f . . . . 
            . . . . . f 5 5 5 5 f . . . . . 
            . . . . . f 5 5 5 5 f . . . . . 
            . . . . . . f f f f . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            . . . . . . . . . . . . . . . . 
            `, SpriteKind.Food)
        scene.place(value, egg)
        animation.runMovementAnimation(
        egg,
        animation.animationPresets(animation.bobbing),
        2000,
        true
        )
    }
}
function create_map () {
    scene.setBackgroundColor(1)
    scene.setTileMap(img`
        9 9 9 . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . . . . . . 5 . . . . . . . . . . 
        . . . . . . . . . . . . 5 . . . . . . . . . . . . . . . . . . . 
        . . . . . . . 5 . . . . . . . . . . . . . 7 7 . . . 5 . . . . . 
        . . . 5 . . . . . . e e e e e . . . . . 7 e e . . . . . . . . . 
        . . . . . . . . . . . . . . . . . 5 . 7 e e e . . 7 7 7 . . . a 
        7 7 7 7 7 . . 7 7 . . . . . . . 7 7 7 e e e e . . e e e . . 7 7 
        e e e e e 2 2 e e 2 2 2 2 2 2 2 e e e e e e e 2 2 e e e 2 2 e e 
        `)
    scene.setTile(7, img`
        7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 
        6 6 7 6 7 6 7 6 6 d 6 7 7 6 7 7 
        d d 6 7 7 6 7 d d d 7 6 d 6 7 6 
        d d d d d d 6 d d d d d d d 6 d 
        d d d d d d d d d d d d d d d d 
        d 1 1 d 1 d d d d d 1 d d d d d 
        d 1 1 d d d d d d d d d d d d d 
        d d d d d d d d d d d d d d d d 
        d d d d d d d d d d d d d d d d 
        d d d d d d b d d d d d d d 1 d 
        d d d d d d d d d d d d d d d d 
        d d b d d d d d d d d b b d d d 
        d d d d d d d d d d d b b d d d 
        d d d d d d d d d d d d d d d d 
        d d d d d d d 1 d d d d d d d d 
        d d d d d d d d d d d d d d 1 d 
        `, true)
    scene.setTile(14, img`
        d 1 d d d d d d d 1 d d d d d d 
        d 1 d d d d d d d 1 d d d d d d 
        d 1 d d d d d d d 1 d d d d d d 
        1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 
        d d d d d 1 d d d d d d d 1 d d 
        d d d d d 1 d d d d d d d 1 d d 
        d d d d d 1 d d d d d d d 1 d d 
        1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 
        d 1 d d d d d d d 1 d d d d d d 
        d 1 d d d d d d d 1 d d d d d d 
        d 1 d d d d d d d 1 d d d d d d 
        1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 
        d d d d d 1 d d d d d d d 1 d d 
        d d d d d 1 d d d d d d d 1 d d 
        d d d d d 1 d d d d d d d 1 d d 
        1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 
        `, true)
    scene.setTile(2, img`
        c c c c c c c c c c c c c c c c 
        8 8 8 8 8 8 8 8 8 8 8 8 8 8 8 8 
        8 8 8 6 6 6 8 8 8 6 6 6 6 8 8 8 
        6 6 8 8 8 6 6 6 6 6 6 8 8 8 8 6 
        6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 
        9 9 6 6 6 6 6 9 9 9 9 6 6 6 9 9 
        6 6 6 6 9 9 9 6 6 6 9 9 9 9 9 9 
        9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 
        9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 
        9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 
        9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 
        9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 
        9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 
        9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 
        9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 
        9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 
        `, true)
    scene.setTile(10, img`
        . . . . . . . . . . . . . . . . 
        . . . . . c . . . . . . . . . . 
        . . . . . f 2 2 . . . . . . . . 
        . . . . . f 2 2 2 2 2 . . . . . 
        . . . . . f 2 2 2 2 2 2 2 2 . . 
        . . . . . f 2 2 2 2 2 2 2 . . . 
        . . . . . f 2 2 2 2 . . . . . . 
        . . . . . f 2 . . . . . . . . . 
        . . . . . f . . . . . . . . . . 
        . . . . . f . . . . . . . . . . 
        . . . . . f . . . . . . . . . . 
        . . . . . f . . . . . . . . . . 
        . . . . . f . . . . . . . . . . 
        . . . . f f f . . . . . . . . . 
        . . . f c c c f . . . . . . . . 
        . . f c c c c c f . . . . . . . 
        `, true)
    scene.setTile(9, img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, false)
    scene.setTile(5, img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, false)
}
function create_stand_animation () {
    anim_stand_right = animation.createAnimation(ActionKind.standing_right, 200)
    anim_stand_right.addAnimationFrame(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . f f f f f f f f . . 
        . . . . 4 f 7 7 7 7 7 7 7 7 f . 
        . . . . 4 f 7 7 7 1 f 1 7 7 f . 
        . . . . f f 7 7 7 1 f 1 7 7 f . 
        . . . . 4 f 7 7 7 1 1 1 7 7 f . 
        . . . 4 4 f 7 7 f 7 7 7 7 7 f . 
        . . . f f 7 7 7 f f f f f f . . 
        . . . 4 f 7 7 7 7 7 7 f . . . . 
        . f 4 4 f 7 f 7 7 7 7 7 7 f . . 
        f 7 7 f 7 7 f 7 7 7 7 7 7 f . . 
        . f 7 7 7 7 7 7 d d 7 f . . . . 
        . . f 7 7 7 7 d d d 7 f . . . . 
        . . . f 7 7 7 d d d 7 f . . . . 
        . . . . f 7 7 f f d 7 f . . . . 
        . . . . f f f . . f f f . . . . 
        `)
    anim_stand_right.addAnimationFrame(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . f f f f f f f f . . 
        . . . . 4 f 7 7 7 7 7 7 7 7 f . 
        . . . . 4 f 7 7 7 1 f 1 7 7 f . 
        . . . . f f 7 7 7 1 f 1 7 7 f . 
        . . . . 4 f 7 7 7 1 1 1 7 7 f . 
        . . . 4 4 f 7 7 f 7 7 7 7 7 f . 
        . . . f f 7 7 7 f f f f f f . . 
        . . . 4 f 7 7 7 7 7 7 f . . . . 
        . . 4 4 f 7 f 7 7 7 7 7 7 f . . 
        . . f f 7 7 f 7 7 7 7 7 7 f . . 
        . 4 4 f 7 7 7 7 d d 7 f . . . . 
        4 f f 7 7 7 7 d d d 7 f . . . . 
        f 7 7 7 7 7 7 d d d 7 f . . . . 
        f f f f f 7 7 f f d 7 f . . . . 
        . . . . f f f . . f f f . . . . 
        `)
    anim_stand_left = animation.createAnimation(ActionKind.standing_left, 200)
    anim_stand_left.addAnimationFrame(img`
        . . . . . . . . . . . . . . . . 
        . . f f f f f f f f . . . . . . 
        . f 7 7 7 7 7 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f f . . . . 
        . f 7 7 1 1 1 7 7 7 f 4 . . . . 
        . f 7 7 7 7 7 f 7 7 f 4 4 . . . 
        . . f f f f f f 7 7 7 f f . . . 
        . . . . f 7 7 7 7 7 7 f 4 . . . 
        . . f 7 7 7 7 7 7 f 7 f 4 4 f . 
        . . f 7 7 7 7 7 7 f 7 7 7 7 7 f 
        . . . . f 7 d d 7 7 7 7 7 7 f . 
        . . . . f 7 d d d 7 7 7 7 f . . 
        . . . . f 7 d d d 7 7 7 f . . . 
        . . . . f 7 d f f 7 7 f . . . . 
        . . . . f f f . . f f f . . . . 
        `)
    anim_stand_left.addAnimationFrame(img`
        . . . . . . . . . . . . . . . . 
        . . f f f f f f f f . . . . . . 
        . f 7 7 7 7 7 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f 4 . . . . 
        . f 7 7 1 f 1 7 7 7 f f . . . . 
        . f 7 7 1 1 1 7 7 7 f 4 . . . . 
        . f 7 7 7 7 7 f 7 7 f 4 4 . . . 
        . . f f f f f f 7 7 7 f f . . . 
        . . . . f 7 7 7 7 7 7 f 4 . . . 
        . . f 7 7 7 7 7 7 f 7 f 4 4 . . 
        . . f 7 7 7 7 7 7 f 7 7 f f . . 
        . . . . f 7 d d 7 7 7 7 f 4 4 . 
        . . . . f 7 d d d 7 7 7 7 f f 4 
        . . . . f 7 d d d 7 7 7 7 7 7 f 
        . . . . f 7 d f f 7 7 f f f f f 
        . . . . f f f . . f f f . . . . 
        `)
    animation.attachAnimation(dino, anim_stand_left)
    animation.attachAnimation(dino, anim_stand_right)
}
scene.onHitTile(SpriteKind.Player, 2, function (sprite) {
    game.over(false)
})
let anim_stand_left: animation.Animation = null
let anim_stand_right: animation.Animation = null
let egg: Sprite = null
let tile_list: tiles.Tile[] = []
let dino: Sprite = null
let anim_walk_right: animation.Animation = null
let anim_walk_left: animation.Animation = null
create_map()
create_dino()
create_eggs()
info.setScore(0)

```



## Step 2
**Step 2**
1. Repeat the same step, create another function call **create_dino**
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_1.png)

### ~ tutorialhint
```blocks
function create_map () {
}

function create_dino () {
}
```
