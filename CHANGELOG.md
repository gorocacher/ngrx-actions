# 2.1.0 - 1/14/18
- Feature: Add support for memoized selectors in `@Select` decorator
- Feature: add support for `@Select('a', 'b', 'c')` in `@Select` decorator
- Fix: Performance improvement on `@Select('a.b.a)` #14

# 2.0.7 - 1/10/18
- Fix: Fix publish

# 2.0.6 - 1/10/18
- Fix: Type issue #13

# 2.0.5 - 1/9/18
- Fix: Performance Improvements #10

# 2.0.4 - 1/7/18
- Feature: Memoize Select

# 2.0.3 - 1/7/18
- Fix: Build tweaks

# 2.0.2 - 1/7/18
- Chore: Add error handling for select connect

# 2.0.1 - 1/7/18
- Chore: Better builds

# 2.0.0 - 1/5/18
- Feature: Implied select name from property name
- BREAKING: Add module for proper DI of selects

Instead of:
```javascript
import { ngrxSelect } from 'ngrx-actions';

@NgModule({
    imports: [NgrxActionsModule]
})
export class AppModule {
    constructor(store: Store<MyState>) {
        ngrxSelect(store);
    }
}
```

do this:

```javascript
import { NgrxActionsModule, NgrxSelect } from 'ngrx-actions';

@NgModule({
    imports: [NgrxActionsModule]
})
export class AppModule {
    constructor(ngrxSelect: NgrxSelect, store: Store<MyState>) {
        ngrxSelect.connect(store);
    }
}
```

# 1.2.0 - 1/3/18
- Feature: Select decorator

# 1.1.3 - 1/3/18
- Fix: Effects mismatch

# 1.1.2 - 1/3/18
- Fix: Effects with normal objects

# 1.1.1 - 1/3/18
- Fix: NPM publish issue

# 1.1.0 - 1/3/18
- Fix: Seralization
- Feature: Support multiple actions

# 1.0.0 - 1/2/18
- Initial Release
