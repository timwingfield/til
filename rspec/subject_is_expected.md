### is_expected in rspec

`:subject` is assumed to be under test unless otherwise specified. You can set up your subject in
different ways:

```
  subject(:user) {User.new}
  
  subject(:briefing) { build_stubbed(:briefing) }
```

This allows you to use the `is_expected` matcher in your tests.

`it { is_expected.to be_valid }`

Or, with the `:briefing` setup:

`it { expects(briefing.name).to eq "name" }`
