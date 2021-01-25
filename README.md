# Deno Markdown Site

A simple static site generator built with Deno.

## Usage

```
deno run --allow-read --unstable --allow-write main.ts example-site.md build
```

## Development

I recommend using [`denon`](https://github.com/denosaurs/denon):

```bash
deno install --allow-read --allow-run --allow-write -f --unstable https://deno.land/x/denon/denon.ts
```

Then you can use

```bash
denon run --allow-read --unstable --allow-write main.ts example-site.md
```

## License

MIT