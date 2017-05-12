## What
This is part of the Phaser Component Library.

A "link" is a player-controlled character than can move on the X and Y axes. It is not affected by gravity, has a given amount of health, uses arrow keys to move, and does not bind the camera to its movement. Based on Link from the Legend of Zelda games.

## How
`npm install phaser-link`

Then, in your Phaser source code

```js
import Link from 'phaser-link'

// in your game creation method:
this.game.physics.startSystem( Phaser.Physics.ARCADE )

// add a controllable (arrow keys) Link-like player character
const link = this.game.add.existing(new Link({
    game: this.game,
    key: 'your-sprite-key',
    controls: true
}))
```

## API

### `new Link( { options } )`

#### options

##### `collideWorldBounds`

Type: `boolean`<br>
Default: `false`

Whether or not the link collides with the world bounds.

##### `controls`

Type: `boolean`<br>
Default: `false`

Whether or not the link can be controlled by the player.

##### `frame`

Type: `string | number`<br>
Default: `''`

See [Sprite docs](https://phaser.io/docs/2.6.2/Phaser.Sprite.html).

##### `game`

Required<br>
Type: `Phaser.Game`

The game where this link will live.

##### `health`

Type: `number`<br>
Default: `1`

This link's starting health.

##### `height`

Type: `number`<br>
Default: `64`

This link's height.

##### `key`

Type: `string | Phaser.RenderTexture | Phaser.BitmapData | PIXI.Texture`<br>
Default: `''`

See [Sprite docs](https://phaser.io/docs/2.6.2/Phaser.Sprite.html).

##### `matchDiagonalSpeed`

Type: `boolean`<br>
Default: `true`

Forces the link's diagonal speed to match its straight-line speed.

The vector of a link's diagonal movement will have a magnitude greather than its speed, making the link move faster diagonally than it moves in a straight line. Set this value to `true` or leave as-is to prevent this behavior.

##### `speed`

Type: `number`<br>
Default: `350`

The speed of the link.

##### `width`

Type: `number`<br>
Default: `64`

This link's width.

##### `x`

Type: `number`<br>
Default: `0`

The x-value of the link's spawn location.

##### `y`

Type: `number`<br>
Default: `0`

The y-value of the link's spawn location.

### Properties

##### `state`

Type: `Phaser.State`

Shortcut to the current state object. Useful for accessing global properties from that state.
