# combigen
An efficient CLI tool to generate possible combinations written in C++

## Introduction
Combigen aims to assist with data generation and exploration. Given a `.json` input where each key contains an array of string values, combigen can either generate every possible combination or a random subset of the possible combinations. It aims to provide memory-efficiency while maintaining high-performance. This can be especially useful when large amounts of data are needed for statistical analysis or mock data in an application.

It supports exporting to `.csv` and `.json`.

## Usage

Basic commands are listed below:


```
Usage: combigen [options]
   -h             Displays this help message

   -a             Generates every possible combination
                  (Note: this should be used with caution when storing to disk)

   -n <index>     Generate combination at nth index

   -i <input>     Take the given .json file as input. Otherwise, input will come
                  from stdin.
                  Example: "{ "foo": [ "a", "b", "c" ], "bar": [ "1", "2" ] }"

   -t <type>      Output type (csv or json). Defaults to csv

   -r <size>      Generate a random sample of size r from
                  the possible set of combinations

   -d <delimiter> Set the delimiter when displaying combinations (default is ',')

   -k             Display the keys on the first line of output (for .csv)

   -v             Display version number
```

## Installation


### Linux/UNIX

1. Clone the repository and `cd` into it:

```
$ git clone https://github.com/iamtheburd/combigen.git && cd combigen
```

2. Build with `make`:

```
$ make
```

3. Install:

```
$ sudo make install
```

Alternatively, you can also check out the [Releases](https://github.com/iamtheburd/combigen/releases) tab and directly download the `combigen` binary from there.

### Windows


1. Download Visual Studio and install first

2. Clone the repository to some directory

3. Open up the Developer Command Prompt (can usually be found by searching in the Start menu)

4. `cd` to where your cloned repository is

5. Build the file:

```
> cl src\combigen.cpp /EHsc /O2
```

6. Place the resulting `combigen.exe` wherever you desire

Alternatively, you can also check out the [Releases](https://github.com/iamtheburd/combigen/releases) tab and directly download the `combigen.exe` from there.

## Third-Party Libraries

Combigen uses the following open-source libraries:

* [nlohmann/json](https://github.com/nlohmann/json) - An excellent C++ library for parsing JSON

* [iamtheburd/lazy-cartesian-product](https://github.com/iamtheburd/lazy-cartesian-product) - Small C++ library I developed to generate the combinations

* [skandhurkat/Getopt-for-Visual-Studio](https://github.com/skandhurkat/Getopt-for-Visual-Studio) - Port of the MinGW version of `getopt.h` so that the CLI works on Windows


## Contributing
Pull-requests are always welcome!

## License
Licensed under GPLv3, see [LICENSE](https://github.com/iamtheburd/blob/master/LICENSE)
