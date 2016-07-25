![Screenshot](https://samme.github.io/phaser-plugin-scene-graph/screenshot.png)
# Phaser Scene Graph Plugin 👾

Prints Phaser’s display tree in the console.
[Demo](https://samme.github.io/phaser-plugin-scene-graph/).

    game.plugins.add(Phaser.Plugin.SceneGraph);

    game.debug.graph() // everything; or

    game.debug.graph(obj) // 1 object & descendants

    game.debug.graph(obj, { // options:
        collapse:        true,
        filter:          null, // function (obj) -> true | false
        map:             null, // function (obj) -> "description"
        skipDead:        false,
        skipNonexisting: false
    });

## Tips

    // Name your groups and emitters:

    group.name = "invaders"

    emitter.name = "stars"


For a quick look at a game in progress, run in the console:

    (this.game || Phaser.GAMES[0]).load.script("SceneGraph",
        "https://samme.github.io/phaser-plugin-scene-graph/SceneGraph.js",
        function (){
            this.game.plugins.add(Phaser.Plugin.SceneGraph).graph();
        }).start();
