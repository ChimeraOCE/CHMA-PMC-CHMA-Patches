# CHMA PMC Patches

Custom **Arma Reforger patch and insignia addon** for **Chimera PMC (CHMA)**.

This addon provides CHMA-specific patches and insignia for use across compatible uniforms, equipment and other assets used by the unit.

## Dependencies

The following Arma Reforger addons are required:

* **RHS - Content Pack 01**
* **RHS - Status Quo**
* **RHS - Content Pack 02**

These dependencies must be installed and enabled in Arma Reforger Workbench when developing, modifying or testing the addon.

Do not remove these dependencies unless all resources that rely on them have also been removed from the project.

## Development

This addon is developed using the **Arma Reforger Workbench**.

Clone the repository directly into your local Arma Reforger addons directory:

```text
Documents\My Games\ArmaReforger\addons\CHMA-PMC-CHMA-Patches
```

Open the project's `.gproj` file through Arma Reforger Workbench.

When opening a freshly cloned copy of the project, allow Workbench to build its local resource database before making changes.

The following Workbench-generated file is deliberately excluded from Git:

```text
resourceDatabase.rdb
```

This file is generated locally and should not be committed to the repository.

## Modifying

The addon should remain focused on **CHMA patches, insignia and their associated Reforger assets**.

When adding or modifying patches:

1. Add the source texture to the appropriate existing directory.
2. Follow the existing naming convention for CHMA assets.
3. Generate or update the required Reforger texture resources in Workbench.
4. Create or update the relevant material, prefab or patch definition.
5. Check all resource references before committing.
6. Test the patch on the equipment it is intended to be used with.

Where possible, extend or inherit existing assets rather than duplicating complete third-party assets.

Do not modify RHS or other third-party addon source files directly.

If additional third-party content becomes required, add the relevant project as a dependency rather than copying its content into this repository.

## Adding New Patches

When adding a new CHMA patch:

* Use a clean source image with appropriate transparency.
* Keep image dimensions consistent with existing patch assets where practical.
* Use descriptive and consistent resource names.
* Check the orientation of the patch in-game.
* Check both left and right mounting positions where applicable.
* Confirm the patch remains readable at normal gameplay distances.
* Avoid unnecessarily large texture resolutions.
* Keep any associated `.meta` files with their resources.

When replacing an existing patch, verify that existing prefab and equipment references continue to resolve correctly.

## Testing

Before committing changes:

* Open the project in Workbench without missing-resource errors.
* Check the Workbench console for resource or dependency errors.
* Spawn the affected equipment or uniform.
* Verify the correct patch is displayed.
* Check patch orientation.
* Check patch scale and positioning.
* Test assets that rely on RHS content.
* Test using the normal CHMA Reforger modset where applicable.

Changes affecting equipment used by players should also be tested in multiplayer before release.

## Git

Only files required to develop, build and maintain the addon should be committed.

The following Workbench-generated file is deliberately excluded:

```text
resourceDatabase.rdb
```

Before committing:

* Review all changed files.
* Check for accidentally moved or deleted resources.
* Check for broken resource references.
* Include required `.meta` files.
* Do not commit `resourceDatabase.rdb`.
* Use a commit message that clearly describes the change.

Example commit messages:

```text
Add CHMA Pararescue patch
```

```text
Update CHMA PMC shoulder patch texture
```

```text
Fix patch orientation on RHS uniform
```

## Notes

This repository is intended to act as the central source for **Chimera PMC patch and insignia assets**.

Keep unrelated systems, weapons, vehicles, uniforms and other standalone content in their appropriate CHMA repositories.

If a future change introduces:

* a new dependency;
* an unusual Workbench setup requirement;
* a special testing process; or
* a non-obvious asset relationship;

document it in this README so another CHMA developer can clone the repository, open the project and understand how to continue working on it.
