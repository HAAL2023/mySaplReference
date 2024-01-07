### Policy-Integration-Tests

Instead of testing a single SAPL document, all policies can be tested together using the PDP interface, just like when an application uses an embedded PDP or a SAPL server.

The `SaplIntegrationTestFixture` manages these kinds of integrations tests.

```
    private SaplTestFixture fixture;

    @BeforeEach
    void setUp() {
        fixture = new SaplIntegrationTestFixture("policiesIT")
            .withPDPPolicyCombiningAlgorithm(
                PolicyDocumentCombiningAlgorithm.PERMIT_UNLESS_DENY
            );
    }
```