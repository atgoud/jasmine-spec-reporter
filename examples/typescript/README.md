Use jasmine-spec-reporter with TypeScript
=========================================

## Configuration

```typescript
import {DisplayProcessor, SpecReporter} from "jasmine-spec-reporter";
import SuiteInfo = jasmine.SuiteInfo;

class CustomProcessor extends DisplayProcessor {
    public displayJasmineStarted(info: SuiteInfo, log: string): string {
        return `TypeScript ${log}`;
    }
}

jasmine.getEnv().clearReporters();
jasmine.getEnv().addReporter(new SpecReporter({
    customProcessors: [CustomProcessor],
}));
```

## Example

You can find an example in this directory:

    npm install
    npm test
