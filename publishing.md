# Publishing

This document describes step-by-step how to release a new version of the library to pub.

First install melos via command:

```sh
dart pub global activate melos
```

After you need to bootstrap in order update local dependencies:

```sh
melos bootstrap
```

1. **floor_annotation**
    1. Update CHANGELOG
    1. Update version
    2. Update dependencies
    
2. **floor**
    1. Update CHANGELOG
    2. Update README with updated library versions
    3. Update version
    4. Update dependencies
    
3. **floor_generator**
    1. Update CHANGELOG
    2. Update version
    3. Update dependencies

4. Run `melos bootstrap` again to get all dependencies

4. Check if all dependencies can be resolved and project runs as expected

5. Validate if everything is OK, by running `melos publish --dry-run`

6. To publish all packages run `melos publish --no-dry-run`

7. Update top-level README with updated library versions

8. Update docs/getting-started.md with updated library versions

9. Update docs/changelog.md
  	
10. Create pull request with changes

11. Merge changes into develop branch

12. Create GitHub release
