# Manchester Codes Git-Quest

Git workflow group task.

## Getting started

Choose one member of your group to do these first steps:

Fork and clone this repository. Then add the other members of your group as collaborators, giving them write permission to the repo. 

Open the repository:

```bash
  cd git-quest/
```

Install dependencies:

```bash
  npm install
```

Run tests:

```bash
  npm test
```

Make a dev branch from master: 

```bash
  git checkout -b dev
```

## Challenge

For this challenge you will be working together to add features to a pre-existing code base. Each new set of additions should be made on a separate branch before being merged into `dev`. Take turns with driver and navigator roles to practice the git workflow concepts you've learned. Complete the `pull` and `merge` cycle onto `dev` with each of the following sets of additions: 

### Character

Make these additions to the `Character` prototype:

- Characters should have a `level` property at their construction, unless otherwise stated it should be level 1.

- Characters should have a `baseAttack` and `baseDefense` property at their construction. These should be `0` unless otherwise stated.

- Characters should have a `get attackTotal` and `get defenseTotal` method. It should return the appropriate property added to the `level`. For example `Character.attackTotal()` should return `baseAttack + level`. 

### Enemy

Make these additions to the `Enemy` prototype:

- Enemies no longer need their damage property. Instead, they will  base their damage on the `Character.attackTotal()` method. Re-write the tests to account for this. 

- Enemies should have an `experienceReward` property. If this is not set at construction, it should be `100` by default. 

- Enemies should not be able to attack if they are dead. Add a guard clause to prevent this. 

### Player

Make these additions to the `Player` prototype:

- Players should have a `levelUp` method that increases their `level` by one.

- Players should have a `nextLevel` property at creation, this should be `1000` by default. 

- Players should have a `currentExperience` property at creation, this should be set to `0` by default.

- Players should now calculate the damage dealt to targets as `attackTotal` + `weapon.damage`.

- Change the `Player.attack(target)` method so that a killing blow will add the target's `experienceReward` to the `Player.currentExperience`.

- After a killing blow and experience reward, Players should check if their `currentExperience` is equal to or greater than their `nextLevel` property. If so, the `levelUp()` method should be called, and a new `nextLevel` target that is 10% larger should be set.  




