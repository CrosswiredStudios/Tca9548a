# Tca9548a
.NET (C#) implementation of Tca9548a multiplexer


This is a very simple implementation I wrote for a personal project. The choice to use a static class was made to allow other code to manage the selection, but it could easily be made into a normal class.

## Usage

### When using only one multiplexer that is using the default channel 0x70

```
Tca9548a.Initialize();
Tca9548a.SelectAddress(0x01);
```

### When using multiple multiplexers

```
Tca9548a.Initialize(0x70);
Tca9548a.Initialize(0x71);

Tca9548a.SelectAddress(0x70, 0x01);
// some code

Tca9548a.SelectAddress(0x71, 0x01);
// some other code
```
