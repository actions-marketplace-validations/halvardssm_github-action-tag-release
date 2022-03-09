# tag-release

Create a new GitHub release if package.json version does not exist as a release.

## Usage

Use the action inside your workflow yaml file like this:

```yml
- name: Create Release
  id: release
  uses: halvardssm/github-action-tag-release@v1
  with:
    token: ${{ secrets.GITHUB_TOKEN }}
    path: "./package.json" # optional, will use ./package.json by default
- run: |
    echo 'Release created: ${{steps.version.outputs.release_created}}' # boolean
    echo 'Release exists: ${{steps.version.outputs.release_exists}}' # boolean
```
