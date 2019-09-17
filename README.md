It's not always clear what does `number` or `string` type mean.

Let's imagine you are describing `setTimeout`

```typescript
declare function setTimeout(handler: TimerHandler, timeout?: number, ...arguments: any[]): number;
```

In't not clear what number to pass in `timeout`. Let's refactor it

```typescript
type Milliseconds = number;
declare function setTimeout(handler: TimerHandler, timeout?: Milliseconds, ...arguments: any[]): number;
```

Now it's much more clear, and user will see hints when typing this function in IDE.

So this library is just a set of such aliases. For now it contains

```typescript
export type Milliseconds = number;
export type Seconds = number;
export type Minutes = number;
export type Hours = number;
export type Days = number;
export type Months = number;
export type Years = number;
export type Centuries = number;
```

So use it to clarify your inputs!
