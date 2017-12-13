<div class="jumbotron" id="commands">
  <h1>Command List</h1>
  <p>This page is a list of all commands, subcommands, and valid arguments that Avrae can parse.</p>
  <p>Avrae's command system is split into distinct modules. All commands are called by starting a message with the message prefix (default <kbd>!</kbd>, but can be configured), followed by the command name.</p>
  <p><small>This list is current as of Build 330.</small></p>
</div>
<div class="row" id="chargen">
  <h2>CharGen</h2>
  <p>A random character generator. This module is not integrated into SheetManager, it's meant to be used as a reference while creating character sheets.</p>
  <table class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>Command</th>
        <th>Description</th>
        <th>Syntax</th>
        <th>Arguments</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>makechar</td>
        <td>Generates stats for a 5e character with defined race/class/background.</td>
        <td>!makechar &lt;level&gt;</td>
        <td><kbd>level</kbd> - What level to generate the character.</td>
      </tr>
      <tr>
        <td>randchar</td>
        <td>Generates stats for a random 5e character.</td>
        <td>!randchar [level]</td>
        <td><kbd>level</kbd> (optional) - What level to make the character. If not specified, will return a stat array.</td>
      </tr>
    </tbody>
  </table>
</div>
<div class="row" id="core">
  <h2>Core</h2>
  <p>Core utilities and miscellaneous non-D&amp;D commands.</p>
  <table class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>Command</th>
        <th>Description</th>
        <th>Syntax</th>
        <th>Arguments</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>about</td>
        <td>Prints information about the bot.</td>
        <td>!about, !stats, !info</td>
        <td>None</td>
      </tr>
      <tr>
        <td>bug</td>
        <td>Reports a bug to the bot developer.</td>
        <td>!bug &lt;report&gt;, !feedback &lt;report&gt;</td>
        <td><kbd>report</kbd> - The bug report.</td>
      </tr>
      <tr>
        <td>donate</td>
        <td>Prints a link to donate to the bot developer.</td>
        <td>!donate</td>
        <td>None</td>
      </tr>
      <tr>
        <td>invite</td>
        <td>Prints a link to invite Avrae to your server.</td>
        <td>!invite</td>
        <td>None</td>
      </tr>
      <tr>
        <td>ping</td>
        <td>Checks Avrae's ping time to Discord.</td>
        <td>!ping</td>
        <td>None</td>
      </tr>
    </tbody>
  </table>
</div>
<div class="row" id="customization">
  <h2>Customization</h2>
  <p>Commands to help streamline using Avrae through command shortcuts.</p>
  <table class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>Command</th>
        <th>Description</th>
        <th>Syntax</th>
        <th>Arguments</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>alias</td>
        <td>Adds an alias for a long command.<br>
          After an alias has been added, you can instead run the aliased command by calling it with the bot prefix, followed by the alias name.<br>
          <!--For more details, see <a href="./aliases.html">Alias and Snippet Tutorial</a>.--></td>
        <td>
          <p>Basic Usage: !alias &lt;alias_name&gt; [commands]</p>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Subcommand</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>list</td>
                <td>Lists all aliases.</td>
                <td>!alias list</td>
              </tr>
              <tr>
                <td>remove</td>
                <td>Removes an alias.</td>
                <td>!alias remove &lt;alias_name&gt;</td>
              </tr>
            </tbody>
          </table>
        </td>
        <td><kbd>alias_name</kbd> - The name of the alias.<br>
          <kbd>commands</kbd> (optional) - The commands that the alias is a shortcut of. Do not include the bot prefix. If not provided, prints what the alias is.</td>
      </tr>
      <tr>
        <td>multiline</td>
        <td>Runs each line as a separate command, with a 1 second delay between commands.</td>
        <td>!multiline &lt;commands&gt;</td>
        <td><kbd>commands</kbd> - The commands to run. Ex: <pre>!multiline<br>!roll 1d20<br>!spell Fly<br>!monster Rat</pre></td>
      </tr>
    </tbody>
  </table>
</div>
<div class="row" id="dice">
  <h2>Dice</h2>
  <p>Widely-used miscellaneous dice and math commands.</p>
  <table class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>Command</th>
        <th>Description</th>
        <th>Syntax</th>
        <th>Arguments</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>cast</td>
        <td>Casts a spell (i.e. rolls all the dice and displays a summary [auto-deleted after 15 sec]).</td>
        <td>!cast &lt;spell_name&gt; [args]</td>
        <td>
          <kbd>spell_name</kbd> - The name of the spell.<br>
          <kbd>args</kbd> (optional) - See table.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Arg</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>-r</td>
                <td>Rolls the following dice instead of the default.</td>
                <td>-r &lt;dice&gt;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>iterroll</td>
        <td>Rolls dice a certain number of times, counting successes.</td>
        <td>!iterroll, !rrr &lt;iterations&gt; &lt;dice&gt; [dc]</td>
        <td><kbd>iterations</kbd> - The number of times to reroll the dice.<br>
            <kbd>dice</kbd> - The dice to roll.<br>
            <kbd>dc</kbd> (Optional) - The minimum roll for a result to be a success. If not supplied, assumes 0.</td>
      </tr>
      <tr>
        <td>monster_atk</td>
        <td>Rolls a monster's attack.</td>
        <td>!monster_atk, !ma &lt;monster_name&gt; [atk_name] [args]</td>
        <td><kbd>monster_name</kbd> - The name of the monster.<br>
            <kbd>atk_name</kbd> (Optional) - The name of the monster's attack. If not supplied, prints a list of all of the monster's attacks.<br>
            <kbd>args</kbd> (Optional) - See table.<br><br>
            <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Arg</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>adv/dis</td>
                <td>Rolls the attack at advantage/disadvantage.</td>
                <td>adv/dis</td>
              </tr>
              <tr>
                <td>-ac</td>
                <td>Rolls the attack against a set AC.</td>
                <td>-ac &lt;ac&gt;</td>
              </tr>
              <tr>
                <td>-b</td>
                <td>Adds a bonus to the attack roll.</td>
                <td>-b &lt;bonus&gt;</td>
              </tr>
              <tr>
                <td>-d</td>
                <td>Adds extra dice to the damage roll.</td>
                <td>-d &lt;dice&gt;</td>
              </tr>
              <tr>
                <td>-d#</td>
                <td>Adds extra dice to the first <kbd>#</kbd> attacks that hit.</td>
                <td>-d# &lt;dice&gt;</td>
              </tr>
              <tr>
                <td>-rr</td>
                <td>Rolls the attack multiple times.</td>
                <td>-rr &lt;times to reroll&gt;</td>
              </tr>
              <tr>
                <td>-t</td>
                <td>Sets the attack's target.</td>
                <td>-t &lt;target&gt;</td>
              </tr>
              <tr>
                <td>-phrase</td>
                <td>Sets the attack's flavor text.</td>
                <td>-phrase &lt;text&gt;</td>
              </tr>
              <tr>
                <td>crit</td>
                <td>Makes the attack automatically crit.</td>
                <td>crit</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>multiroll</td>
        <td>Rolls dice a certain number of times, adding together the totals.</td>
        <td>!multiroll, !rr &lt;iterations&gt; &lt;dice&gt;</td>
        <td><kbd>iterations</kbd> - The number of times to reroll the dice.<br>
            <kbd>dice</kbd> - The dice to roll.</td>
      </tr>
      <tr>
        <td>roll</td>
        <td>Rolls dice.</td>
        <td>!roll, !r &lt;dice&gt;</td>
        <td>
          <kbd>dice</kbd> - The dice to roll. Avrae will automatically distinguish between dice and comments, separating it in output. Rolls can be annotated with comments in brackets (e.g. <code>!r 1d20[To Hit]</code>). See Operators and Selectors table below.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Operator</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>k</td>
                <td>Keeps certain dice.</td>
                <td>(dice)k(selector)<br>
                    Ex: <code>!r 2d20kh1</code></td>
              </tr>
              <tr>
                <td>ro</td>
                <td>Rerolls certain dice once.</td>
                <td>(dice)ro(selector)<br>
                    Ex: <code>!r 2d6ro1</code></td>
              </tr>
              <tr>
                <td>rr</td>
                <td>Rerolls certain dice forever.</td>
                <td>(dice)rr(selector)<br>
                    Ex: <code>!r 2d6rr1</code></td>
              </tr>
              <tr>
                <td>mi/ma</td>
                <td>Sets minimum/maximum roll.</td>
                <td>(dice)mi/ma(number)<br>
                    Ex: <code>!r 3d8mi2</code></td>
              </tr>
              <tr>
                <td>adv/dis</td>
                <td>Rolls with advantage/disadvantage.</td>
                <td>(dice) adv/dis<br>
                    Ex: <code>!r 1d20 adv</code></td>
              </tr>
            </tbody>
          </table>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Selector</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>l#</td>
                <td>Selects the lowest <kbd>#</kbd> dice.</td>
                <td>(dice)(operator)l#<br>
                    Ex: <code>!r 2d20kl1</code></td>
              </tr>
              <tr>
                <td>h#</td>
                <td>Selects the highest <kbd>#</kbd> dice.</td>
                <td>(dice)(operator)h#<br>
                    Ex: <code>!r 4d6kh3</code></td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
    </tbody>
  </table>
</div>
<div class="row" id="help">
  <h2>Help</h2>
  <p>For some reason, !help has it's own module. Don't ask.</p>
  <table class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>Command</th>
        <th>Description</th>
        <th>Syntax</th>
        <th>Arguments</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>help</td>
        <td>Prints the help message.</td>
        <td>!help [command]</td>
        <td><kbd>command</kbd> (Optional) - If passed, shows the usage of a certain command. Otherwise, prints the generic help message.</td>
      </tr>
    </tbody>
  </table>
</div>
<div class="row" id="inittracker">
  <h2>InitTracker</h2>
  <p>Commands to help track initiative through a dynamic combat tracker. Every command here is invoked with <kbd>!init</kbd> or <kbd>!i</kbd> followed by the command name.</p>
  <table class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>Command</th>
        <th>Description</th>
        <th>Syntax</th>
        <th>Arguments</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>begin</td>
        <td>Begins combat in the channel.</td>
        <td>!init begin [args]</td>
        <td>
          <kbd>args</kbd> (Optional) - See table. <br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Arg</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>-dyn</td>
                <td>Enables dynamic initiative. If this is enabled, each combatant's initiative will be rerolled at the top of each round.</td>
                <td>-dyn</td>
              </tr>
              <tr>
                <td>--name</td>
                <td>Names the combat.</td>
                <td>--name &lt;name&gt;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>add</td>
        <td>Adds a generic combatant to combat.<br>
            If a character is set up with the SheetManager module, you can use <kbd>cadd</kbd> instead.<br>
            If you are adding monsters to combat, you can use <kbd>madd</kbd> instead.</td>
        <td>!init add &lt;modifier&gt; &lt;name&gt; [args]</td>
        <td>
          <kbd>modifier</kbd> - The combatant's initiative modifier.<br>
          <kbd>name</kbd> - The combatant's name.<br>
          <kbd>args</kbd> (Optional) - See table.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Arg</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>-h</td>
                <td>Hides combatant's HP and AC.</td>
                <td>-h</td>
              </tr>
              <tr>
                <td>-p</td>
                <td>Sets combatant's initiative to <code>modifier</code> instead of rolling.</td>
                <td>-p</td>
              </tr>
              <tr>
                <td>--controller</td>
                <td>Sets the combatant's controller (who is pinged on the combatant's turn).</td>
                <td>--controller &lt;@controller&gt;</td>
              </tr>
              <tr>
                <td>--group</td>
                <td>Adds the combatant to a group. Creates the group if it doesn't exist.</td>
                <td>--group &lt;group name&gt;</td>
              </tr>
              <tr>
                <td>--hp</td>
                <td>Sets the combatant's max HP.</td>
                <td>--hp &lt;max hp&gt;</td>
              </tr>
              <tr>
                <td>--ac</td>
                <td>Sets the combatant's AC.</td>
                <td>--ac &lt;AC&gt;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>cadd</td>
        <td>Adds the current active character to combat, allowing integrated attacks to be used. A character must be loaded through the SheetManager module first.</td>
        <td>!init cadd, !init dcadd [args]</td>
        <td>
          <kbd>args</kbd> (Optional) - See table.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Arg</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>adv/dis</td>
                <td>Rolls the initiative check at advantage/disadvantage.</td>
                <td>adv/dis</td>
              </tr>
              <tr>
                <td>-b</td>
                <td>Adds a bonus to the initiative check.</td>
                <td>-b &lt;dice&gt;</td>
              </tr>
              <tr>
                <td>-phrase</td>
                <td>Sets the check's flavor text.</td>
                <td>-phrase &lt;text&gt;</td>
              </tr>
              <tr>
                <td>-p</td>
                <td>Places the combatant at a certain initiative instead of rolling.</td>
                <td>-p &lt;init&gt;</td>
              </tr>
              <tr>
                <td>-h</td>
                <td>Hides combatant's HP and AC.</td>
                <td>-h</td>
              </tr>
              <tr>
                <td>--group</td>
                <td>Adds the combatant to a group. Creates the group if it doesn't exist.</td>
                <td>--group &lt;group name&gt;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>update</td>
        <td>Updates a combatant's sheet if they were added with <kbd>cadd</kbd>.</td>
        <td>!init update &lt;combatant&gt;</td>
        <td><kbd>combatant</kbd> - The name of the combatant to update.</td>
      </tr>
      <tr>
        <td>madd</td>
        <td>Adds a monster to combat, allowing integrated attacks to be used.</td>
        <td>!init madd &lt;monster_name&gt; [args]</td>
        <td>
          <kbd>monster_name</kbd> - The name of the monster to add.<br>
          <kbd>args</kbd> (Optional) - See table.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Arg</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>adv/dis</td>
                <td>Rolls the initiative check at advantage/disadvantage.</td>
                <td>adv/dis</td>
              </tr>
              <tr>
                <td>-b</td>
                <td>Adds a bonus to the initiative check.</td>
                <td>-b &lt;dice&gt;</td>
              </tr>
              <tr>
                <td>-n</td>
                <td>Adds more than one monster to combat. If <code>--name</code> is not specfied, names combatants as the first two letters followed by a number.</td>
                <td>-n &lt;number of monsters&gt;</td>
              </tr>
              <tr>
                <td>-p</td>
                <td>Places the combatant at a certain initiative instead of rolling.</td>
                <td>-p &lt;init&gt;</td>
              </tr>
              <tr>
                <td>--name</td>
                <td>Sets the name of the combatants added. Any <kbd>#</kbd>s will be automatically replaced with incrementing numbers, starting at 1. Ex: <code>Orc#</code> will add Orc1, Orc2, etc.</td>
                <td>--name &lt;name scheme&gt;</td>
              </tr>
              <tr>
                <td>-h</td>
                <td>Unhides combatant's HP and AC.</td>
                <td>-h</td>
              </tr>
              <tr>
                <td>--group</td>
                <td>Adds the combatant to a group. Creates the group if it doesn't exist.</td>
                <td>--group &lt;group name&gt;</td>
              </tr>
              <tr>
                <td>-npr</td>
                <td>Adds the combatant without physical (bludgeoning, slashing, and piercing) resistances, immunities, or vulnerabilities. Usually used for parties with a lot of magical weapons.</td>
                <td>-npr</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>next</td>
        <td>Moves to the next turn in initiative order.<br>
            It must be your turn or you must be the DM (the user who started combat) to use this command.</td>
        <td>!init next, !init n</td>
        <td>None</td>
      </tr>
      <tr>
        <td>list</td>
        <td>Prints a summary of all combatants in combat.</td>
        <td>!init list</td>
        <td>None</td>
      </tr>
      <tr>
        <td>note</td>
        <td>Adds a note to a combatant.</td>
        <td>!init note &lt;combatant&gt; [note]</td>
        <td>
          <kbd>combatant</kbd> - The name of the combatant to add a note to.<br>
          <kbd>note</kbd> (Optional) - The note to add. If not given, removes all notes.
        </td>
      </tr>
      <tr>
        <td>opt</td>
        <td>Edits the options of a combatant.</td>
        <td>!init opt, !init opts &lt;combatant&gt; &lt;args&gt;</td>
        <td>
          <kbd>combatant</kbd> - The name of the combatant to edit.<br>
          <kbd>args</kbd> - See table.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Arg</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>-h</td>
                <td>Toggles the hidden status of the combatant.</td>
                <td>-h</td>
              </tr>
              <tr>
                <td>-p</td>
                <td>Changes the combatant's initiative value.</td>
                <td>-p &lt;init&gt;</td>
              </tr>
              <tr>
                <td>--controller</td>
                <td>Changes the controller of the combatant (the user who is pinged).</td>
                <td>--controller &lt;@controller&gt;</td>
              </tr>
              <tr>
                <td>--ac</td>
                <td>Changes the combatant's AC.</td>
                <td>--ac &lt;AC&gt;</td>
              </tr>
              <tr>
                <td>--resist</td>
                <td>Adds a resistance to the combatant, for use with integrated attacks.</td>
                <td>--resist &lt;damage type&gt;</td>
              </tr>
              <tr>
                <td>--immune</td>
                <td>Adds an immunity to the combatant, for use with integrated attacks.</td>
                <td>--immune &lt;damage type&gt;</td>
              </tr>
              <tr>
                <td>--vuln</td>
                <td>Adds a vulnerability to the combatant, for use with integrated attacks.</td>
                <td>--vuln &lt;damage type&gt;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>sim</td>
        <td>Simulates one turn of combat. Requires all combatants to be added with either <code>!init madd</code> or <code>!init cadd</code>. Any MonsterCombatant will attack any CharacterCombatant, and vice versa.</td>
        <td>!init sim</td>
        <td>None</td>
      </tr>
      <tr>
        <td>status</td>
        <td>Prints the status of a combatant.</td>
        <td>!init status &lt;combatant&gt; [args]</td>
        <td>
          <kbd>combatant</kbd> - The name of the combatant to print the status of.<br>
          <kbd>args</kbd> (Optional) - If <code>private</code> is passed, PMs the user the status.
        </td>
      </tr>
      <tr>
        <td>hp</td>
        <td>Sets/modifies a combatant's HP.</td>
        <td>!init hp &lt;combatant&gt; &lt;operator&gt; &lt;hp&gt;</td>
        <td>
          <kbd>combatant</kbd> - The name of the combatant to damage/heal.<br>
          <kbd>operator</kbd> - Either <code>mod</code> (modify hp), <code>set</code> (set hp), or <code>max</code> (set max hp).<br>
          <kbd>hp</kbd> - The HP value to set/modify by.
        </td>
      </tr>
      <tr>
        <td>effect</td>
        <td>Adds a status effect to a combatant.</td>
        <td>!init effect &lt;combatant&gt; &lt;duration&gt; &lt;effect&gt;</td>
        <td>
          <kbd>combatant</kbd> - The name of the combatant to add an effect to.<br>
          <kbd>duration</kbd> - The duration, in rounds, of the status effect. If infinite, this should be <code>-1</code>.<br>
          <kbd>effect</kbd> - The name of the effect.
        </td>
      </tr>
      <tr>
        <td>re</td>
        <td>Removes a status effect from a combatant.</td>
        <td>!init re &lt;combatant&gt; [effect]</td>
        <td>
          <kbd>combatant</kbd> - The name of the combatant to remove an effect from.<br>
          <kbd>effect</kbd> (Optional) - The name of the effect to remove. If not given, removes all effects.
        </td>
      </tr>
      <tr>
        <td>attack</td>
        <td>Rolls an integrated attack by the current combatant against another combatant. Only works if the combatant was added with <kbd>cadd</kbd> or <kbd>madd</kbd>. Automatically determines target HP, AC, resistances, immunities, and vulnerabilities.</td>
        <td>!init attack, !init a &lt;target&gt; &lt;weapon&gt; [args]</td>
        <td>
          <kbd>target</kbd> - The name of the target.<br>
          <kbd>weapon</kbd> - The name of the attack.<br>
          <kbd>args</kbd> (Optional) - See table for <code>!attack</code> if combatant was added with <code>cadd</code>, or <code>!monster_atk</code> if combatant was added with <code>madd</code>.
        </td>
      </tr>
      <tr>
        <td>remove</td>
        <td>Removes a combatant from combat.</td>
        <td>!init remove &lt;combatant&gt;</td>
        <td>
          <kbd>combatant</kbd> - The name of the combatant to remove.
        </td>
      </tr>
      <tr>
        <td>end</td>
        <td>Ends combat in a channel.</td>
        <td>!init end</td>
        <td>None</td>
      </tr>
    </tbody>
  </table>
</div>
<div class="row" id="lookup">
  <h2>Lookup</h2>
  <p>Commands to look up items, spells, status effects, monsters, etc.</p>
  <table class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>Command</th>
        <th>Description</th>
        <th>Syntax</th>
        <th>Arguments</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>condition</td>
        <td>Looks up a condition or status effect, such as <code>Grappled</code>.</td>
        <td>!condition, !status &lt;name&gt;</td>
        <td>
          <kbd>name</kbd> - The name of the condition to look up.
        </td>
      </tr>
      <tr>
        <td>item</td>
        <td>Looks up an item, such as <code>Longsword</code> or <code>Deck of Many Things</code>.</td>
        <td>!item &lt;item_name&gt;</td>
        <td>
          <kbd>item_name</kbd> - The name of the item to look up.
        </td>
      </tr>
      <tr>
        <td>lookup_settings</td>
        <td>Changes the lookup settings in a server.<br>
            Note: A GM role is any role named "GM", "Game Master", "DM", or "Dungeon Master."</td>
        <td>!lookup_settings &lt;args&gt;</td>
        <td>
          <kbd>args</kbd> - See table.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Arg</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>-req_dm_monster</td>
                <td>Toggles whether a GM role is required to show the full stat block of a monster.</td>
                <td>-req_dm_monster [true/false]</td>
              </tr>
              <tr>
                <td>-pm_result</td>
                <td>Toggles whether the output of a lookup is PMed instead of printed.</td>
                <td>-pm_result [true/false]</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>monster</td>
        <td>Looks up a monster, such as <code>Ancient Silver Dragon</code>. If user looking up is not a GM, will show a generalization (this can be toggled).</td>
        <td>!monster &lt;monster_name&gt;</td>
        <td>
          <kbd>monster_name</kbd> - The name of the monster to look up.
        </td>
      </tr>
      <tr>
        <td>spell</td>
        <td>Looks up a spell, such as <code>Invisibility</code>.</td>
        <td>!spell &lt;spell_name&gt;</td>
        <td>
          <kbd>spell_name</kbd> - The name of the spell to look up.
        </td>
      </tr>
      <tr>
        <td>rule</td>
        <td>Looks up a rule, such as <code>Exhaustion</code> or <code>Grapple</code>.</td>
        <td>!rule &lt;rule_name&gt;</td>
        <td>
          <kbd>rule_name</kbd> - The name of the rule to look up.
        </td>
      </tr>
    </tbody>
  </table>
</div>
<div class="row" id="pbputils">
  <h2>PBPUtils</h2>
  <p>Commands to streamline playing-by-post over Discord.</p>
  <table class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>Command</th>
        <th>Description</th>
        <th>Syntax</th>
        <th>Arguments</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>br</td>
        <td>Prints a scene break (horizontal line).</td>
        <td>!br</td>
        <td>None</td>
      </tr>
      <tr>
        <td>echo</td>
        <td>Echoes a message.</td>
        <td>!echo &lt;msg&gt;</td>
        <td>
          <kbd>msg</kbd> - The message to echo.
        </td>
      </tr>
      <tr>
        <td>embed</td>
        <td>Generates and prints an embed.</td>
        <td>!embed &lt;args&gt;</td>
        <td>
          <kbd>args</kbd> - See table.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Arg</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>-title</td>
                <td>Sets the title of the embed.</td>
                <td>-title &lt;title&gt;</td>
              </tr>
              <tr>
                <td>-desc</td>
                <td>Sets the description of the embed.</td>
                <td>-desc &lt;description text&gt;</td>
              </tr>
              <tr>
                <td>-thumb</td>
                <td>Sets the image URL displayed in the thumbnail.</td>
                <td>-thumb &lt;image url&gt;</td>
              </tr>
              <tr>
                <td>-image</td>
                <td>Sets the image URL.</td>
                <td>-image &lt;image url&gt;</td>
              </tr>
              <tr>
                <td>-footer</td>
                <td>Sets the text of the footer.</td>
                <td>-footer &lt;footer text&gt;</td>
              </tr>
              <tr>
                <td>-color</td>
                <td>Sets the color of the embed.</td>
                <td>-color &lt;hex code&gt;</td>
              </tr>
              <tr>
                <td>-f</td>
                <td>Adds a field to the embed. This can be called multiple times.</td>
                <td>-f &lt;"Field Title|Field Text"&gt;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>pythag</td>
        <td>Performs a Pythagorean theorem calculation to calculate diagonals.</td>
        <td>!pythag &lt;num1&gt; &lt;num2&gt;</td>
        <td>
          <kbd>num1</kbd> - The first number.<br>
          <kbd>num2</kbd> - The second number.
        </td>
      </tr>
    </tbody>
  </table>
</div>
<div class="row" id="permissions">
  <h2>Permissions</h2>
  <p>Commands to manage the bot's command system. Each setting is server-specific.</p>
  <table class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>Command</th>
        <th>Description</th>
        <th>Syntax</th>
        <th>Arguments</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>disable</td>
        <td>Disables a command for a server. Requires Manage Server permissions.</td>
        <td>!disable &lt;command&gt;</td>
        <td>
          <kbd>command</kbd> - The name of the command to disable.
        </td>
      </tr>
      <tr>
        <td>enable</td>
        <td>Enables a command for a server. Requires Manage Server permissions.</td>
        <td>!enable &lt;command&gt;</td>
        <td>
          <kbd>command</kbd> - The name of the command to enable.
        </td>
      </tr>
      <tr>
        <td>prefix</td>
        <td>Sets the bot's prefix for a server. Requires Manage Server permissions.<br><br>
            Forgot the prefix? Reset it with <code>@Avrae#6944 prefix !</code>.</td>
        <td>!prefix [prefix]</td>
        <td>
          <kbd>prefix</kbd> (Optional) - The new prefix. If not given, displays the current prefix.
        </td>
      </tr>
    </tbody>
  </table>
</div>
<div class="row" id="sheetmanager">
  <h2>SheetManager</h2>
  <p>Commands to import a character sheet from <a href="https://dicecloud.com/">Dicecloud</a> or <a href="https://www.reddit.com/r/dndnext/comments/2iyydv/5th_edition_editable_pdf_character_sheets/">a PDF</a>, generating macros for attacks, saves, and checks.</p>
  <table class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>Command</th>
        <th>Description</th>
        <th>Syntax</th>
        <th>Arguments</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>attack</td>
        <td>Rolls an attack for the currently active character.</td>
        <td>!attack, !a &lt;atk_name&gt; [args]</td>
        <td>
          <kbd>atk_name</kbd> - The name of the attack.<br>
          <kbd>args</kbd> (Optional) - See table.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Arg</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>adv/dis</td>
                <td>Rolls the attack at advantage/disadvantage.</td>
                <td>adv/dis</td>
              </tr>
              <tr>
                <td>-ac</td>
                <td>Rolls the attack against a set AC.</td>
                <td>-ac &lt;ac&gt;</td>
              </tr>
              <tr>
                <td>-b</td>
                <td>Adds a bonus to the attack roll.</td>
                <td>-b &lt;bonus&gt;</td>
              </tr>
              <tr>
                <td>-d</td>
                <td>Adds extra dice to the damage roll.</td>
                <td>-d &lt;dice&gt;</td>
              </tr>
              <tr>
                <td>-d#</td>
                <td>Adds extra dice to the first <kbd>#</kbd> attacks that hit.</td>
                <td>-d# &lt;dice&gt;</td>
              </tr>
              <tr>
                <td>-rr</td>
                <td>Rolls the attack multiple times.</td>
                <td>-rr &lt;times to reroll&gt;</td>
              </tr>
              <tr>
                <td>-t</td>
                <td>Sets the attack's target.</td>
                <td>-t &lt;target&gt;</td>
              </tr>
              <tr>
                <td>-c</td>
                <td>Adds extra dice to a crit..</td>
                <td>-c &lt;dice&gt;</td>
              </tr>
              <tr>
                <td>-phrase</td>
                <td>Sets the attack's flavor text.</td>
                <td>-phrase &lt;text&gt;</td>
              </tr>
              <tr>
                <td>-title</td>
                <td>Sets the attack's title. If <code>[charname]</code>, <code>[aname]</code>, or <code>[target]</code> is supplied, it will be automatically replaced.</td>
                <td>-title &lt;text&gt;</td>
              </tr>
              <tr>
                <td>-resist</td>
                <td>Sets the target's resistances for automatic dice halving.</td>
                <td>-resist &lt;damage type&gt;</td>
              </tr>
              <tr>
                <td>-immune</td>
                <td>Sets the target's immunities for automatic dice zeroing.</td>
                <td>-immune &lt;damage type&gt;</td>
              </tr>
              <tr>
                <td>-vuln</td>
                <td>Sets the target's vulnerabilities for automatic dice doubling.</td>
                <td>-vuln &lt;damage type&gt;</td>
              </tr>
              <tr>
                <td>crit</td>
                <td>Makes the attack automatically crit.</td>
                <td>crit</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>character</td>
        <td>Switches the active character.</td>
        <td>!character, !char [name] [args]</td>
        <td>
          <kbd>name</kbd> - The name of the character to switch to.<br>
          <kbd>args</kbd> - If <code>delete</code> is given, deletes the character.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Subcommand</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>list</td>
                <td>Lists all characters.</td>
                <td>!char list</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>check</td>
        <td>Rolls an ability check for the active character.</td>
        <td>!check, !c &lt;check&gt; [args]</td>
        <td>
          <kbd>check</kbd> - The name of the check to roll.<br>
          <kbd>args</kbd> (Optional) - See table.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Arg</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>adv/dis</td>
                <td>Rolls the check at advantage/disadvantage.</td>
                <td>adv/dis</td>
              </tr>
              <tr>
                <td>-b</td>
                <td>Adds a bonus to the check roll.</td>
                <td>-b &lt;bonus&gt;</td>
              </tr>
              <tr>
                <td>-mc</td>
                <td>Sets the minimum roll of the d20.</td>
                <td>-mc &lt;min&gt;</td>
              </tr>
              <tr>
                <td>-phrase</td>
                <td>Sets the check's flavor text.</td>
                <td>-phrase &lt;text&gt;</td>
              </tr>
              <tr>
                <td>-title</td>
                <td>Sets the check's title. If <code>[charname]</code> or <code>[cname]</code> is supplied, it will be automatically replaced.</td>
                <td>-title &lt;text&gt;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>csettings</td>
        <td>Updates settings for the active character.</td>
        <td>!csettings &lt;args&gt;</td>
        <td>
          <kbd>args</kbd> - See table.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Subcommand</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>color</td>
                <td>Colors all embeds this color.</td>
                <td>!csettings color &lt;hex color&gt;</td>
              </tr>
              <tr>
                <td>criton</td>
                <td>Makes attacks crit on a roll other than a 20.</td>
                <td>!csettings criton &lt;number&gt;</td>
              </tr>
              <tr>
                <td>reroll</td>
                <td>Defines a number that a check will automatically reroll on, for cases such as Halfling Luck.</td>
                <td>!csettings reroll &lt;number&gt;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>cvar</td>
        <td>Commands to manage character variables for use in snippets and aliases. Character variables can be called in the -phrase tag by surrounding the variable name with <code>{}</code> (calculates) or <code>&lt;&gt;</code> (prints). Dicecloud <code>statMod</code> and <code>statScore</code> variables are also available.</td>
        <td>!cvar &lt;var_name&gt; [value]</td>
        <td>
          <kbd>var_name</kbd> - The name of the variable.<br>
          <kbd>value</kbd> - The value of the variable. If not given, prints the current value.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Subcommand</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>remove</td>
                <td>Deletes a cvar.</td>
                <td>!cvar remove &lt;var_name&gt;</td>
              </tr>
              <tr>
                <td>list</td>
                <td>Lists all of the character's cvars.</td>
                <td>!cvar list</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>desc</td>
        <td>Prints the description of your currently active character.</td>
        <td>!desc</td>
        <td>None</td>
      </tr>
      <tr>
        <td>dicecloud</td>
        <td>Loads a character sheet from <a href="https://dicecloud.com/">Dicecloud</a>.</td>
        <td>!dicecloud &lt;url&gt;</td>
        <td>
          <kbd>url</kbd> - The URL of the character sheet.
        </td>
      </tr>
      <tr>
        <td>pdfsheet</td>
        <td>Loads a character sheet from <a href="https://www.reddit.com/r/dndnext/comments/2iyydv/5th_edition_editable_pdf_character_sheets/">this</a> PDF.</td>
        <td>!pdfsheet (must be called in the same message the sheet is uploaded)</td>
        <td>None</td>
      </tr>
      <tr>
        <td>portrait</td>
        <td>Shows the image of the currently active character.</td>
        <td>!portrait</td>
        <td>None</td>
      </tr>
      <tr>
        <td>save</td>
        <td>Rolls a saving throw for the currently active character.</td>
        <td>!save, !s &lt;skill&gt; [args]</td>
        <td>
          <kbd>skill</kbd> - The type of saving throw to roll.<br>
          <kbd>args</kbd> (Optional) - See table.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Arg</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>adv/dis</td>
                <td>Rolls the save at advantage/disadvantage.</td>
                <td>adv/dis</td>
              </tr>
              <tr>
                <td>-b</td>
                <td>Adds a bonus to the save roll.</td>
                <td>-b &lt;bonus&gt;</td>
              </tr>
              <tr>
                <td>-phrase</td>
                <td>Sets the save's flavor text.</td>
                <td>-phrase &lt;text&gt;</td>
              </tr>
              <tr>
                <td>-title</td>
                <td>Sets the save's title. If <code>[charname]</code> or <code>[sname]</code> is supplied, it will be automatically replaced.</td>
                <td>-title &lt;text&gt;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>sheet</td>
        <td>Prints the character sheet of the currently active character.</td>
        <td>!sheet</td>
        <td>None</td>
      </tr>
      <tr>
        <td>snippet</td>
        <td>Creates a snippet to use in attack, save, and check macros.</td>
        <td>!snippet &lt;snipname&gt; [snippet]</td>
        <td>
          <kbd>snipname</kbd> - The name of the snippet.<br>
          <kbd>snippet</kbd> (Optional) - The arguments the snippet is a shortcut of. If not passed, prints the value of the snippet.<br><br>
          <table class="table table-striped table-bordered">
            <thead>
              <tr>
                <th>Subcommand</th>
                <th>Description</th>
                <th>Syntax</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>remove</td>
                <td>Deletes a snippet.</td>
                <td>!snippet remove &lt;snipname&gt;</td>
              </tr>
              <tr>
                <td>list</td>
                <td>Lists all snippets.</td>
                <td>!snippet list</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
      <tr>
        <td>update</td>
        <td>Updates the current character sheet, preserving all settings.</td>
        <td>!update [args]</td>
        <td>
          <kbd>args</kbd> (Optional) - If <code>-h</code> is passed, will hide the character sheet.
        </td>
      </tr>
    </tbody>
  </table>
</div>
