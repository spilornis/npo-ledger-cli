Non-Profit Accounting With Ledger CLI, A Tutorial
=================================================

Non-profit organizations (NPOs), particularly 501(c)(3) charities in the USA,
have their own specific accounting needs.  These often differ from for-profit
accounting needs.  For example, for-profit-oriented systems often make
problematic assumptions about the workflow of accounting tasks (often because
NPOs rely primarily on donations, rather than fee-for-service or
widget-selling income).  Also, non-profit income is categorized differently
than for-profit income, and the reporting requirements vary wildly from their
for-profit equivalents.

This project is designed to provide some basic templates, tutorials, workflow
documentation and scripts to handle accounting for an NPO.  The primary
example is a
[direct project (aka Model A) fiscal sponsor NPO](http://en.wikipedia.org/wiki/Fiscal_sponsorship#Models_of_fiscal_sponsorship).

This tutorial was written primarily based on
[Software Freedom Conservancy](http://sfconservancy.org/)'s use of Ledger CLI
from 2008-10-22 to present for its own accounting needs.  While Conservancy
has done well using this system, and believes that its account system meets
Generally accepted accounting principles (GAAP), this document **does not**
constitute advice from a CPA nor legal advice for a non-profit that seeks to
comply with relevant state and/or federal accounting requirements for USA
non-profits.  The authors make no representations nor warranties regarding
this information and this information is provided for discussion purposes
only.  Readers of these tutorial and templates are urged to seek professional
advice from a CPA and/or tax legal counsel in constructing an accounting
system appropriate for your organization.

Furthermore, given the authors' limited knowledge of accounting requirements
outside the USA, the suggestions herein probably are not particularly useful
at all for organizations outside the USA.

Configuration of Chart of Accounts
----------------------------------

The first thing any accountant will ask to see if your so-called "chart of
accounts".  The first time I heard this phrase, I thought it was something
complicated.  Fact of the matter is, it's really just a list of all the
accounts that you use.  Accountants also use "account codes", which, as near
as I can tell, are of primary interest because they get better sorting.
Ledger CLI doesn't really support account codes, so I've ignored them.

The real place that Ledger CLI stores your chart of accounts is if you use
the `account` directive along with the `--pedantic` CLI option.  This will
ensure that only accounts you declared explicitly will used.

### Asset Accounts

Our recommendation for asset accounts FIXME.


### Reporting The Chart of Accounts

The
[`general-ledger-report.plx` script in the `non-profit-audit-reports` Ledger CLI contrib directory](https://github.com/ledger/ledger/blob/next/contrib/non-profit-audit-reports/general-ledger-report.plx)
will generate a file called `chart-of-accounts.csv`, which is the chart of accounts.

Copyright and License of This File
----------------------------------

This specific document, the README.md file for npo-ledger-cli, is copyrighted:
  Copyright &copy; 2013, Bradley M. Kuhn

This document's license gives you freedom; you can copy, modify, convey,
propagate, and/or redistribute this software under the terms of either:

    * The GNU General Public License as published by the Free Software
      Foundation, Inc.; either version 3 of the License, or (at your option)
      any later version (aka GPLv3-or-later).

    * *or* the Creative Commons Attribution-ShareAlike 3.0 United States
      license, as published by Creative Commons, Inc. (aka CC-By-SA-USA-3.0)

In addition, when you convey, distribute, and/or propagate this document
and/or modified versions thereof, you may also preserve this notice so that
recipients of such distributions will also have both licensing options
described above.

A copy of GPLv3 and CC-By-SA-3.0-USA can be found in the same repository as
this file under the filenames GPLv3.txt and CC-By-SA-3.0-USA.txt.  If this
document has been separated from the repository, a
[copy of GPL can be found on FSF's website](http://www.gnu.org/licenses/gpl.txt)
and a
[copy of CC-By-SA-USA-3.0 can be found on Creative Commons' website](http://creativecommons.org/licenses/by-sa/3.0/us/legalcode).
