# Contributing to MeetMage Extensions

Thanks for helping improve MeetMage extensions. Bug reports, feature ideas and pull requests are all welcome.

## Reporting bugs

Open an issue in the extension's repository using the **Bug report** template. Please include:

- Magento / Adobe Commerce version and edition
- PHP version
- Theme (Hyvä, Luma or custom) and Hyvä version if relevant
- Extension version
- Steps to reproduce, expected result and actual result
- Relevant logs from `var/log/` (remove any customer data first)

Security issues must **not** be reported in public issues. See [SECURITY.md](SECURITY.md).

## Pull requests

1. Fork the repository and create a branch from `main`.
2. Follow the [Magento 2 coding standard](https://github.com/magento/magento-coding-standard) and keep code upgrade-safe (plugins, observers and DI preferences, no core overrides).
3. Add or update unit tests for your change.
4. Run the checks locally:
   ```bash
   vendor/bin/phpcs --standard=Magento2 src/
   vendor/bin/phpstan analyse src/ --level=6
   vendor/bin/phpunit tests/
   ```
5. Keep Hyvä and Luma behaviour in sync: if you change a frontend template, check both.
6. Describe what changed and why in the pull request, and link the related issue.

## Commit messages

Use short, imperative subjects, e.g. `Fix canonical URL for configurable products`.

## License

By contributing, you agree that your contributions are licensed under the MIT License.
