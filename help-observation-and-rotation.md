## Changing the observation bell

The observation bell is the bell whose position is used to name the calling positions. For example, a call at **H**
(Home) is the call that leaves the observation bell in its home position, and a call at **W** leaves it in the Wrong
position. Most compositions use the tenor as observation, but some are easier to read using another bell, for example
in tenors-parted compositions or where a different bell is unaffected in a multi-part.

### Viewing a composition with a different observation bell

When you are signed in, the **Layout** section of a composition page includes the **Alternative observation bell** button (the eye icon). Select it to choose how the composition is presented:

- **Composition** shows the composition as it was entered.
- Each bell of the stage is listed. The composition's own observation bell is marked *(composition)*, and a tick shows
  the bell currently in use.

When you choose a different bell, the composition is laid out again with calling positions named relative to that bell.
The rows rung are exactly the same; only the presentation changes. The button is highlighted while an alternative bell
is in use, and the **Copy** options copy the composition as it is currently presented.

The footnote under the layout names the observation bell, for example *2nd observation*. If the observation bell is not
in the same position at every parthead, it is described as observation *in first part*.

#### Multi-part compositions

In a multi-part composition, the chosen bell may only be at home at some of the partheads. In that case the composition is
presented with fewer parts, and the footnote explains this, for example:

> 6 part presented as a 3 part with the 2nd observation

If the parts cannot be regrouped evenly, the composition is presented as a one-part.

If the composition cannot be laid out with the chosen bell at all, a warning is shown, for example *This composition
cannot be laid out using the 7 as observation*, and the original layout is kept.

### Setting the observation bell when editing

On the **General** tab of the composition editor, the **Observation bell** setting can be:

- a bell of the stage (bells above 9 are shown with their symbol, e.g. *10 (0)*, *11 (E)*). The tenor is the default
  for a new composition.
- **None**, for compositions that don't use named calling positions, e.g. those called only by lead number or with no
  calls.

Default calling positions (such as **W**, **M**, **H**, **B**) are interpreted relative to the observation bell. If you
change it, check that the calling still pricks the composition you intend.

Notes:

- If no observation bell is specified and the calling uses lettered calling positions, the editor warns that the tenor is
  assumed.
- When a composition is saved, an observation bell that isn't needed by the calling (no calls, or numbered positions
  only) is changed to **None**.

### Searching by observation bell

The composition search includes an **Observation bell** filter: *Any*, *None*, *Tenor*, *Not tenor*, or (once a stage
is selected) a specific bell.

---

## Rotating the composition

A composition that starts and finishes with rounds can be started from any of its rows. The **Rotate** transform rewrites
the composition so that it rings exactly the same changes, and has the same length, but starts from a different point.
The new starting row becomes rounds, so all the rows are transposed accordingly.

### Rotating a composition

Rotation is in the **Transforms** row at the bottom of the **General** tab of the composition editor:

> Transforms: Rotate composition to row [&nbsp;&nbsp;&nbsp;] or by [&nbsp;&nbsp;&nbsp;] changes **Apply**

Either:

- enter a **row** of the composition to start from, e.g. `13527486`. If the row occurs more than once (in a
  multi-extent composition), the first occurrence is used. The message reports how many changes the composition was
  rotated by, and the row box is cleared; or
- enter a **number of changes** to rotate by. A negative number rotates the other way, so rotating by `6` and then by
  `-6` returns to the original.

If a row is entered, the number of changes is ignored. Then select **Apply**. The calling table, calling and other
fields are updated in the editor, and the composition is re-pricked so that its properties and layout reflect the new
start. **Nothing is saved until you save the composition**, so you can review the result first.

### What changes

- **Start:** the composition starts at the chosen row. If that is part way through a lead, the start row is set
  accordingly.
- **Observation bell:** if the composition has an observation bell, the new observation bell is the bell that is in
  the old observation bell's position in the rotation row. A message reports the change. A composition with no
  observation bell (**None**) keeps none.
- **Partheads, coursehead masks and calling positions** are transposed to match the new start.
- **Calling and method calling** are rotated. Named blocks are redefined at their first complete use, and part-includes
  are renumbered for the part in which the rotation starts. Where the structure can't be kept, the calling, or a named
  block, is written out in full, and a message tells you.
- **Parts:** the composition may be presented with a different number of parts, e.g. as a one-part. A message tells you
  if this happens.
- **Handstroke/backstroke:** rotating by an odd number of changes doesn't change the *Backstroke start* setting. A message
  reminds you to check whether it should.

The title, notes and other details are not changed, so check whether any of them need updating.

### Reverting a rotation

After a rotation, a **Revert last rotation** button appears. It restores the composition as it was before the rotation.
The button disappears once you make any other change to the composition. You can also rotate back by the same number of
changes in the opposite direction.

### When a composition can't be rotated

**Apply** is unavailable (hover over it to see why) unless the composition:

- has no errors in the editor;
- is a round block; and
- finishes at the same position in a lead as it starts.

A rotation is also refused if:

- the row entered does not occur in the composition;
- the rotation point falls within a call. The message suggests the nearest numbers of changes that can be used instead;
  or
- no calling can be found that rings the rotated composition correctly *and* can be represented in the calling table.
  This can happen with some complex callings, such as part-includes within named blocks. A **Details** section can be
  expanded to show the closest calling that was found.
