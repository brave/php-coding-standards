PHP_CodeSniffer ruleset for Brave.com
=====================================

# Installation

1. Install [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer).
2. Clone the dependent coding standards:

       git clone https://github.com/sirbrillig/phpcs-variable-analysis
       git clone https://github.com/Automattic/VIP-Coding-Standards
       git clone https://github.com/WordPress/WordPress-Coding-Standards
2. Look for the latest release of the [WordPress](https://github.com/WordPress/WordPress-Coding-Standards/releases) and [VIP](https://github.com/Automattic/VIP-Coding-Standards/releases) coding standards and use it instead of the default branch:
       cd WordPress-Coding-Standards ; git checkout 2.3.0
       cd VIP-Coding-Standards ; git checkout 2.2.0

3. Install the dependent coding standards, for example, by creating the
   appropriate symlinks in `/usr/share/php/PHP/CodeSniffer/src/Standards/`:

       cd /usr/share/php/PHP/CodeSniffer/src/Standards/
       sudo ln -s /home/username/phpcs-variable-analysis/VariableAnalysis/ .
       sudo ln -s /home/username/VIP-Coding-Standards/WordPress-VIP-Go/ .
       sudo ln -s /home/username/devel/VIP-Coding-Standards/WordPressVIPMinimum/ .
       sudo ln -s /home/username/devel/WordPress-Coding-Standards/WordPress .
       sudo ln -s /home/username/devel/WordPress-Coding-Standards/WordPress-Core/ .
       sudo ln -s /home/username/devel/WordPress-Coding-Standards/WordPress-Extra .
       sudo ln -s /home/username/devel/WordPress-Coding-Standards/WordPress-Docs .
4. Install the `brave.com` coding standards:

       cd /usr/share/php/PHP/CodeSniffer/src/Standards/
       sudo ln -s /home/username/php-coding-standards/BraveMinimum/ .

# Usage

Create a `phpcs.xml` file in the root of your PHP plugin, similar to this
one:

```
<?xml version="1.0"?>
<ruleset name="PluginName">
	<description>Coding standard for the Plugin-Name plugin</description>

	<rule ref="BraveMinimum">
	</rule>
</ruleset>
```

and then run `phpcs .`.
