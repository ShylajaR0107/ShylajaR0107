**Running the Magical Arena program:**
- Ensure you have Java installed on your system.
- Download the provided MagicalArena.java file.
- Open a terminal and navigate to the directory where MagicalArena.java is located.
- Compile the program by running the following command:

**Copy code:**

javac MagicalArena.java

- After successful compilation, run the program with the following command:

**Copy code:**

java MagicalArena

- The program will simulate a magical arena fight between two players, displaying the actions and outcomes.

**Unit Tests:**
Unit tests can be added to ensure the correctness and robustness of the solution. Below are some examples of possible unit tests:


**Copy code:**

import static org.junit.Assert.assertEquals;

import org.junit.Test;

public class MagicalArenaTest

{

    @Test
    public void testPlayerCreation() {
        Player player = new Player("Test", 100, 20, 15);
        assertEquals("Test", player.getName());
        assertEquals(100, player.getHealth());
        assertEquals(20, player.getStrength());
        assertEquals(15, player.getAttack());
    }

    @Test
    public void testDiceRoll() {
        Dice dice = new Dice(6);
        int roll = dice.roll();
        assertTrue(roll >= 1 && roll <= 6);
    }

    @Test
    public void testAttackDamage() {
        Player player = new Player("Test", 100, 20, 15);
        int damage = player.getAttackDamage(6); // Assuming max roll of 6
        assertEquals(90, damage); // 15 * 6 = 90
    }

    @Test
    public void testDefendDamage() {
        Player player = new Player("Test", 100, 20, 15);
        int damage = player.getDefendDamage(3); // Assuming roll of 3
        assertEquals(60, damage); // 20 * 3 = 60
    } }

These tests cover various aspects of the program, such as player creation, dice rolling, attack damage calculation, and defend damage calculation.

Ensure you have a testing framework like JUnit set up in your development environment to execute these tests.
