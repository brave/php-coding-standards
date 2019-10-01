PHP_CodeSniffer ruleset for Brave.com
=====================================

# Installation

1. Install [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer).
2. Clone the dependent coding standards:

    git clone https://github.com/Automattic/VIP-Coding-Standards
    git clone https://github.com/WordPress/WordPress-Coding-Standards
3. Install the dependent coding standards, for example, by creating the
   appropriate symlinks in `/usr/share/php/PHP/CodeSniffer/src/Standards/`:

    cd /usr/share/php/PHP/CodeSniffer/src/Standards/
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
