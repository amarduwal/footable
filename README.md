# Footable

![Footable](../master/footable.jpg)

FooTable is a jQuery plugin that aims to make HTML tables on smaller devices look awesome - No matter how many columns of data you may have in them.

# What Does It Do?

FooTable transforms your HTML tables into expandable responsive tables. This is how it works:
* It hides certain columns of data at different resolutions (we call these breakpoints).
* Rows become expandable to show the data that was hidden.
So simple! So all the data that is hidden can always be seen just by clicking the row.

## Installation

Footable depends on jQuery. Add this line to your application's Gemfile:

```ruby
gem 'jquery-rails'
gem 'footable'
```

And then execute:

```console
$ bundle install
```

Require Footable Javascripts in app/assets/javascripts/application.js:

```js
//= require jquery
//= require footable
//= require footable.sortable
```

Import Footable styles in `app/assets/stylesheets/application.scss`:

```scss
@import "footable";
@import "footable.sortable"
```

## Usage

Example Usage:
HTML
```html
<table class="footable">
	<thead>
		<tr>
			<th data-class="expand" data-sort-initial="true"><span
			title="table sorted by this column on load">Order ID</span></th>
			<th data-hide="phone,tablet" data-sort-ignore="true">No. of items</th>
			<th data-hide="phone,tablet" data-sort-ignore="true">Invoice</th>
			<th data-hide="phone,tablet"><strong>Payment Method</strong></th>
			<th data-hide="phone,tablet"><strong></strong></th>
			<th data-hide="default"> Price</th>
			<th data-hide="default" data-type="numeric"> Date</th>
			<th data-hide="phone" data-type="numeric"> Status</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>#028DE</td>
			<td>5
				<small>item(s)</small>
			</td>
			<td><a target="_blank">-</a></td>
			<td>Bank Wire</td>
			<td><a href="" class="btn btn-primary btn-sm">view status</a></td>
			<td>$403</td>
			<td data-value="78025368997">22 Jun 2019</td>
			<td data-value="3"><span class="label label-success">Done</span></td>
		</tr>
		<tr>
			<td>#045YU</td>
			<td>2
				<small>item(s)</small>
			</td>
			<td><a target="_blank">-</a></td>
			<td>Bank Wire</td>
			<td><a href="" class="btn btn-primary btn-sm">view status</a></td>
			<td>$105</td>
			<td data-value="-100297281571">28 Oct 2019</td>
			<td data-value="1"><span class="label label-primary">Pending</span></td>
		</tr>
		<tr>
			<td>#08UJL</td>
			<td>6
				<small>item(s)</small>
			</td>
			<td><a target="_blank">-</a></td>
			<td><a target="_blank">PayPal</a></td>
			<td><a href="" class="btn btn-primary btn-sm">view status</a></td>
			<td><a target="_blank">$550 </a></td>
			<td data-value="370961043292">3 Oct 2019</td>
			<td data-value="2"><span class="label label-success">Done</span></td>
		</tr>
		<tr>
			<td>#09ydo</td>
			<td>1
				<small>item(s)</small>
			</td>
			<td><a target="_blank">-</a></td>
			<td>Paypal</td>
			<td><a href="" class="btn btn-primary btn-sm">view status</a></td>
			<td>$34</td>
			<td data-value="-22133780420">19 Apr 2019</td>
			<td data-value="1"><span class="label label-primary">Pending</span></td>
		</tr>
		<tr>
			<td>#EC089</td>
			<td>8
				<small>item(s)</small>
			</td>
			<td><a target="_blank">-</a></td>
			<td>MasterCard</td>
			<td><a href="" class="btn btn-primary btn-sm">view status</a></td>
			<td>$1108</td>
			<td data-value="250833505574">13 Dec 2019</td>
			<td data-value="3"><span class="label label-danger">Cancel</span></td>
		</tr>
		<tr>
			<td>#OH746</td>
			<td>4
				<small>item(s)</small>
			</td>
			<td><a target="_blank">-</a></td>
			<td>Bank Wire</td>
			<td><a href="" class="btn btn-primary btn-sm">view status</a></td>
			<td>$669</td>
			<td data-value="694116650726">30 Dec 2019</td>
			<td data-value="3"><span class="label label-danger">Cancel</span></td>
		</tr>
		<tr>
			<td>#04628J</td>
			<td>11
				<small>item(s)</small>
			</td>
			<td><a target="_blank">-</a></td>
			<td>Bank Wire</td>
			<td><a href="" class="btn btn-primary btn-sm">view status</a></td>
			<td>$400</td>
			<td data-value="561440464855">17 Oct 2019</td>
			<td data-value="2"><span class="label label-default">Disable</span></td>
		</tr>
		<tr>
			<td>#046738</td>
			<td>2
				<small>item(s)</small>
			</td>
			<td><a target="_blank">-</a></td>
			<td><a target="_blank">PayPal</a></td>
			<td><a href="" class="btn btn-primary btn-sm">view status</a></td>
			<td>$403</td>
			<td data-value="437400551390">11 Nov 2019</td>
			<td data-value="3"><span class="label label-danger">Cancel</span></td>
		</tr>		
	</tbody>
</table>
```

Javascript
```js
$(function () {
    $('.footable').footable();
});
```

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/amarduwal/footable. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the Footable project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/amarduwal/footable/blob/master/CODE_OF_CONDUCT.md).
