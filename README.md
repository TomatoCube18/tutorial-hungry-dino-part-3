### @explicitHints true
 
# tutorial



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


## Step 3
** Step 3**
1. Follow the below image, drag the blocks from ``||Loops:on start||`` block to the two function blocks respectively.
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_3.gif)

### ~ tutorialhint
```blocks
function create_map () {
    scene.setBackgroundColor(1)
    scene.setTileMap(img`
        9 9 9 . . . . . . . . . . . . . . . . . . . . . 5 . . . . . . . 
        . . . . . . . . . . . . 5 . 5 . . . . . . . 5 . . . . . . . . . 
        . . . . . . . . . . . 5 . 5 . . . . . 5 . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . . . . . . 7 7 . . . 5 . . . . . 
        . . . 5 . . . . . . d d d d d . . . . . 7 e e . . . . . . . . . 
        . . . . . . . . . . . . . . . . . . . 7 e e e . . 7 7 7 . . . a 
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
    scene.setTile(13, img`
        d 1 1 1 1 1 1 b d 1 1 1 1 1 1 b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d d 1 d d d d d d d 
        b b b b b b d e b b b b b b d e 
        d 1 1 1 1 1 1 b d 1 1 1 1 1 1 b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d d 1 d d d d d d d 
        b b b b b b d e d b b b b b b e 
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
}

```


## Step 4
** Step 4**
1. Open the ``||scene.Functions||`` drawer, drag the ``||scene.create_map||`` into the ``||Loops:on start||`` block.
3. Next, drag the ``||scene.create_dino||`` into the ``||Loops:on start||`` block.

**Testing**: Test out your game, it should work the same as last week.
### ~ tutorialhint
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_12.png)


## Step 5
** Step 5**
1. Click on the tilemap that you have created last week. Let's add Yellow tile to it it.
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_4.gif)

### ~ tutorialhint
```blocks

function create_map () {
    scene.setBackgroundColor(1)
    scene.setTileMap(img`
        9 9 9 . . . . . . . . . . . . . . . . . . . . . 5 . . . . . . . 
        . . . . . . . . . . . . 5 . 5 . . . . . . . 5 . . . . . . . . . 
        . . . . . . . . . . . 5 . 5 . . . . . 5 . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . . . . . . 7 7 . . . 5 . . . . . 
        . . . 5 . . . . . . d d d d d . . . . . 7 e e . . . . . . . . . 
        . . . . . . . . . . . . . . . . . . . 7 e e e . . 7 7 7 . . . a 
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
    scene.setTile(13, img`
        d 1 1 1 1 1 1 b d 1 1 1 1 1 1 b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d d 1 d d d d d d d 
        b b b b b b d e b b b b b b d e 
        d 1 1 1 1 1 1 b d 1 1 1 1 1 1 b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d d 1 d d d d d d d 
        b b b b b b d e d b b b b b b e 
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
```




## Step 6
** Step 6**
1. Open the ``||scene.Functions||`` drawer, click on **Make a Function...**
3. Rename **doSomething** to **create_eggs** 
4. Open the ``||scene.Functions||`` drawer, drag the ``||scene.create_eggs||`` into the ``||Loops:on start||`` block.
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_6.png)

### ~ tutorialhint
```blocks
create_map()
create_dino()
create_eggs()
function create_eggs () {
}
```



## Step 7
** Step 7**
1. Open the ``||scene.Scene||`` drawer, drag the ``||variables.set tile list to array of all tiles||``  into the ``||scene.create_eggs||`` block
2. Click on the grey color oval, choose **Yellow** color.
3. Open the ``||loops.Loops||`` drawer, drag the ``||loops.for element values of list||`` block into the ``||scene.create_eggs||`` block
4. Click on the **list**, change it to **tile list**

### ~ tutorialhint
```blocks
function create_eggs () {
    tile_list = scene.getTilesByType(5)
    for (let value3 of tile_list) {    	
    }
}
```


## Step 8
** Step 8**
1. Open the ``||sprites.Sprites||`` drawer, drag the  ``||variables.set mySprite||`` inside the ``||loops.for element||`` block
2. Click on the grey color oval, select **Gallery** view. Scroll to find the image of an egg, select it and hit "OK". 
3. Rename the character from **mySprite** to **egg**
4. Change the kind from **Player** to **Food**


### ~ tutorialhint
```blocks
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
    }
}
```



## Step 9
** Step 9**
1. Open the ``||scene.Scene||`` drawer, drag the ``||scene.on top of myTile place mySprite||``  inside the ``||loops.for element||`` block
2. Change **myTile** to **value**
3. Change **mySprite** to **egg**

### ~ tutorialhint
```blocks
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
    }
}
```


## Step 10
** Step 10**
1. Open the ``||animation.Animation||`` drawer, drag the  ``||animation.animate mySprite with fly to center||`` into the ``||scene.create_eggs||`` block
2. Change **mySprite** to **egg**
3. Change **fly to center** to **bobbing (in place)**
4. Click on the loop **OFF** to change it to **ON**

### ~ tutorialhint
```blocks
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
```



## Step 11
** Step 11**
1. Open the ``||info.Info||`` drawer, drag the  ``||info.set score to 0||`` into the``||Loops:on start||`` block
2. Open the ``||sprites.Sprites||`` drawer, drag the  ``||sprites.on sprite of kind Player overlap||`` onto empty area.
3. Change the second kind **Player** to **Food**
4. Open the ``||info.Info||`` drawer, drag the  ``||info.change score by 1||`` into the ``||sprites.on sprite of kind Player overlap||`` block.

### ~ tutorialhint
```blocks
create_map()
create_dino()
create_eggs()
info.setScore(0)
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
})
```


## Step 12
** Step 12**
1. Open the ``||sprites.Sprites||`` drawer, drag the  ``||sprites.destroy mySprite||`` into the ``||sprites.on sprite of kind Player overlap||`` block.
2. Drag the **otherSprite** from  ``||sprites.on sprite of kind Player overlap||`` block onto the **mySprite** 
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_5.gif)


### ~ tutorialhint
```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    otherSprite.destroy()
})
```


## Step 13
** Step 13**
1. Open the ``||music.Music||`` drawer, drag the  ``||music.play sound ba ding||`` into the same block.
2. Change the **ba ding** to any sound of your choice.

### ~ tutorialhint
```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    otherSprite.destroy()
    music.jumpUp.play()
})
```

## Step 14
** Step 14**
1. Open the ``||animation.Animation||`` drawer, drag the ``||variables.set anim to create animation of Walking||`` block into the ``||scene.create_idle_animation||`` block
2. Click on **anim**, rename **anim** to **anim_idle_right** 
3. Click on **Walking**, add a new action **idling_right**
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_8.gif)

### ~ tutorialhint
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_13.png)

## Step 15
** Step 15**
1. Open the ``||animation.Animation||`` drawer, drag the ``||animation.add frame to anim||`` block into the ``||scene.create_idle_animation||`` block
2. Change **anim** to **anim_idle_right** 
3. Click on the grey color ovul, select **Gallery** view. Scroll to find the below image of a idling right dino, select it and hit "OK". 
4. Repeat step 1 - 3, for the other idling right dino.
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_10.png)

### ~ tutorialhint
```blocks
let anim_idle_right: animation.Animation = null
function create_idle_animation () {
    anim_idle_right = animation.createAnimation(ActionKind.idling_right, 100)
    anim_idle_right.addAnimationFrame(img`
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
    anim_idle_right.addAnimationFrame(img`
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
}
```


## Step 16
** Step 16**
1. Open the ``||animation.Animation||`` drawer, drag the ``||variables.set anim to create animation of Walking||`` block into the ``||scene.create_idle_animation||`` block
2. Click on **anim**, rename **anim** to **anim_idle_left** 
3. Click on **Walking**, add a new action **idling_left**
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_9.gif)


### ~ tutorialhint
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_14.png)


## Step 17
** Step 17**
1. Open the ``||animation.Animation||`` drawer, drag the ``||animation.add frame to anim||`` block into the ``||scene.create_idle_animation||`` block
2. Change **anim** to **anim_idle_left** 
3. Click on the grey color ovul, select **Gallery** view. Scroll to find the first image of a idling left dino, select it and hit "OK". 
4. Repeat step 1 - 3, for the other idling left dino.
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/Screenshot_11.png)

### ~ tutorialhint
```blocks
let anim_idle_left: animation.Animation = null
function create_idle_animation () {
anim_idle_left = animation.createAnimation(ActionKind.idling_left, 100)
    anim_idle_left.addAnimationFrame(img`
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
    anim_idle_left.addAnimationFrame(img`
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
}
```



## Step 18
** Step 18**
1. Open the ``||animation.Animation||`` drawer, drag the ``||animation.attach animation anim to sprite mySprite||`` block into the ``||scene.create_idle_animation||`` block
2. Change **mySprite** to **dino** 
3. Change **anim** to **anim_idle_rightt** 
4. Repeat step 1 - 3, for **anim_idle_left**


### ~ tutorialhint
```blocks
function create_idle_animation () {
animation.attachAnimation(dino, anim_idle_right)
animation.attachAnimation(dino, anim_idle_left)
}
```


## Step 19
** Step 19**
1. Open the ``||animation.Animation||`` drawer, drag the ``||animation.activate animation Walking on mySprite||`` into the ``||controller.on Right button pressed ||`` block
2. Change **Walking** to **walking_right** 
3. Change **mySprite** to **dino** 


### ~ tutorialhint
```blocks
controller.right.onEvent(ControllerButtonEvent.Pressed, function () {
    animation.setAction(dino, ActionKind.walking_right)
})
```

## Step 20
** Step 20**
1. Open the ``||animation.Animation||`` drawer, drag the ``||animation.activate animation Walking on mySprite||`` into the ``||controller.on Left button pressed ||`` block
2. Change **Walking** to **walking_left** 
3. Change **mySprite** to **dino** 

### ~ tutorialhint
```blocks
controller.left.onEvent(ControllerButtonEvent.Pressed, function () {
    animation.setAction(dino, ActionKind.walking_left)
})
```


## Step 21
** Step 21**
1. Open the ``||controller.Controller||`` drawer, drag the  ``||controller.on A button pressed ||`` onto an empty area.
2. Change **A** to **Right**
3. Change **pressed** to **released**
4. Open the ``||animation.Animation||`` drawer, drag the ``||animation.activate animation Walking on mySprite||`` into the ``||controller.on Right button released ||`` block
5. Change **Walking** to **idling_right** 
6. Change **mySprite** to **dino** 


### ~ tutorialhint
```blocks
controller.right.onEvent(ControllerButtonEvent.Released, function () {
    animation.setAction(dino, ActionKind.idling_right)
})
```


## Step 22
** Step 22**
1. Open the ``||controller.Controller||`` drawer, drag the  ``||controller.on A button pressed ||`` onto an empty area.
2. Change **A** to **Right**
3. Change **pressed** to **released**
4. Open the ``||animation.Animation||`` drawer, drag the ``||animation.activate animation Walking on mySprite||`` into the ``||controller.on Left button released ||`` block
5. Change **Walking** to **idling_left** 
6. Change **mySprite** to **dino** 


### ~ tutorialhint
```blocks
controller.left.onEvent(ControllerButtonEvent.Released, function () {
    animation.setAction(dino, ActionKind.idling_left)
})
```


## Step 23
** Step 23**
1. Open the ``||animation.Animation||`` drawer, drag the ``||animation.activate animation Walking on mySprite||`` into the ``||scene.create_dino ||`` block
2. Change **Walking** to **idling_right** 
3. Change **mySprite** to **dino** 



### ~ tutorialhint
```blocks

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
    create_idle_animation()
    create_walking_animation()
    animation.setAction(dino, ActionKind.idling_right)
}
```




## Step 24 @unplugged
** Step 24**
Congratulations! You have completed today's tutorial. 
Test out your game. If it does not work, cross check your code with the below image.

![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/complete01.png)
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/complete02.png)
![screenshots](https://raw.githubusercontent.com/TomatoCube18/tutorial-hungry-dino-part-2-of-3/master/assets/complete03.png)

### ~ tutorialhint
```blocks
enum ActionKind {
    walking_right,
    idling_right,
    idling_left,
    walking_left,
    Idle,
    Jumping,
    action_dying_right,
    action_dying_left,
    Dying
}
let anim_walk_left: animation.Animation = null
let dino: Sprite = null
let anim_walk_right: animation.Animation = null
let anim_idle_right: animation.Animation = null
let anim_idle_left: animation.Animation = null
let egg: Sprite = null
let tile_list: tiles.Tile[] = []
create_map()
create_dino()
create_eggs()
info.setScore(0)
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
    
function create_idle_animation () {
    anim_idle_right = animation.createAnimation(ActionKind.idling_right, 200)
    anim_idle_right.addAnimationFrame(img`
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
    anim_idle_right.addAnimationFrame(img`
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
    anim_idle_left = animation.createAnimation(ActionKind.idling_left, 200)
    anim_idle_left.addAnimationFrame(img`
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
    anim_idle_left.addAnimationFrame(img`
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
    animation.attachAnimation(dino, anim_idle_right)
    animation.attachAnimation(dino, anim_idle_left)
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
    dino.ay = 290
    dino.setFlag(SpriteFlag.StayInScreen, true)
    controller.moveSprite(dino, 50, 0)
    scene.cameraFollowSprite(dino)
    scene.placeOnRandomTile(dino, 9)
    create_idle_animation()    
    create_walking_animation()
    animation.setAction(dino, ActionKind.idling_right)
}
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (dino.isHittingTile(CollisionDirection.Bottom)) {
        dino.vy = -135
    }
})
controller.left.onEvent(ControllerButtonEvent.Pressed, function () {
    animation.setAction(dino, ActionKind.walking_left)
})
controller.right.onEvent(ControllerButtonEvent.Released, function () {
    animation.setAction(dino, ActionKind.idling_right)
})
controller.left.onEvent(ControllerButtonEvent.Released, function () {
    animation.setAction(dino, ActionKind.idling_left)
})
controller.right.onEvent(ControllerButtonEvent.Pressed, function () {
    animation.setAction(dino, ActionKind.walking_right)
})
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    otherSprite.destroy()
    info.changeScoreBy(1)
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
        9 9 9 . . . . . . . . . . . . . . . . . . . . . 5 . . . . . . . 
        . . . . . . . . . . . . 5 . 5 . . . . . . . 5 . . . . . . . . . 
        . . . . . . . . . . . 5 . 5 . . . . . 5 . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . . . . . . 7 7 . . . 5 . . . . . 
        . . . 5 . . . . . . d d d d d . . . . . 7 e e . . . . . . . . . 
        . . . . . . . . . . . . . . . . . . . 7 e e e . . 7 7 7 . . . a 
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
    scene.setTile(13, img`
        d 1 1 1 1 1 1 b d 1 1 1 1 1 1 b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d d 1 d d d d d d d 
        b b b b b b d e b b b b b b d e 
        d 1 1 1 1 1 1 b d 1 1 1 1 1 1 b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d b 1 d d d d d d b 
        1 d d d d d d d 1 d d d d d d d 
        b b b b b b d e d b b b b b b e 
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
scene.onHitTile(SpriteKind.Player, 2, function (sprite) {
game.over(false, effects.blizzard)
})
scene.onHitTile(SpriteKind.Player, 10, function (sprite) {
    game.over(true)
})
```



> Open this page at [https://tomatocube18.github.io/tutorial-hungry-dino-part-3/](https://tomatocube18.github.io/tutorial-hungry-dino-part-3/)

## Use as Extension

This repository can be added as an **extension** in MakeCode.

* open [https://arcade.makecode.com/](https://arcade.makecode.com/)
* click on **New Project**
* click on **Extensions** under the gearwheel menu
* search for **https://github.com/tomatocube18/tutorial-hungry-dino-part-3** and import

## Edit this project ![Build status badge](https://github.com/tomatocube18/tutorial-hungry-dino-part-3/workflows/MakeCode/badge.svg)

To edit this repository in MakeCode.

* open [https://arcade.makecode.com/](https://arcade.makecode.com/)
* click on **Import** then click on **Import URL**
* paste **https://github.com/tomatocube18/tutorial-hungry-dino-part-3** and click import

## Blocks preview

This image shows the blocks code from the last commit in master.
This image may take a few minutes to refresh.

![A rendered view of the blocks](https://github.com/tomatocube18/tutorial-hungry-dino-part-3/raw/master/.github/makecode/blocks.png)

#### Metadata (used for search, rendering)

* for PXT/arcade
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
