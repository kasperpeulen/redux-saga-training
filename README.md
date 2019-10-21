# Iterator

We call an object an `Iterator` if it implements the following interface.

```typescript
interface Iterator<T> {
  next(): { value: T; done: boolean };
}
```

Becoming a super hero is a fairly straight forward process:

```typescript
class Naturals implements Iterator<number> {
  private i = 0;

  next() {
    this.i++;
    return { value: this.i, done: false };
  }
}

```

