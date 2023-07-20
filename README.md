# runing-images-from-registry-in-gh-action

This action uses an image already stored in some registry, avoiding the repeated build every time the action is called.

Args was used, which overwrites cmd, directly accessing the command necessary to generate the art in the terminal.

If the cmd of your image is already configured, just use the entrypoint that the action has:

```yaml
[...]
runs:
  using: 'docker'
  image: 'docker://quay.io/your/image:v1'
  entrypoint: 'your commands here'
```
## Reference

- [Metadata syntax for GitHub Actions - runs for Docker container actions](https://docs.github.com/en/actions/creating-actions/metadata-syntax-for-github-actions#runs-for-docker-container-actions)

## License

See [LICENSE](LICENSE)
