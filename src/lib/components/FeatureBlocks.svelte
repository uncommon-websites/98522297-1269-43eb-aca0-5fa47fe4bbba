<script lang="ts">
	import FeatureBlock from './FeatureBlock.svelte';
</script>

<!-- Block 1: Payment Initiation -->
<FeatureBlock 
	title="Payment Initiation" 
	description="Enable instant, high-speed, low-fee payments directly from bank accounts with Open Banking compliance."
	buttons={[
		{ text: "EXPLORE PAYMENTS", icon: true },
		{ text: "VIEW DOCS" }
	]}
>
	<div class="w-full h-full bg-white border border-border rounded shadow-sm p-6 font-mono text-xs">
		<div class="flex items-center justify-between border-b border-border pb-3 mb-4">
			<span class="text-muted">PAYMENT REQUEST</span>
			<span class="text-green-600 text-[10px] bg-green-50 px-2 py-1 rounded">AUTHORIZED</span>
		</div>
		<div class="space-y-3">
			<div class="flex justify-between items-center">
				<span class="text-muted">Amount</span>
				<span class="font-semibold">£250.00</span>
			</div>
			<div class="flex justify-between items-center">
				<span class="text-muted">From</span>
				<span class="font-semibold">****4532</span>
			</div>
			<div class="flex justify-between items-center">
				<span class="text-muted">Status</span>
				<div class="flex items-center gap-2">
					<span class="w-2 h-2 bg-green-500 rounded-full"></span>
					<span>Processing</span>
				</div>
			</div>
		</div>
	</div>
</FeatureBlock>

<!-- Block 2: Transactions -->
<FeatureBlock 
	title="Transactions" 
	description="Access up to 2 years of transaction history with merchant details, categories, and real-time webhook notifications."
	buttons={[
		{ text: "VIEW TRANSACTIONS API", icon: true }
	]}
	alignRight={true}
>
	<div class="w-full max-w-md bg-white border border-border rounded shadow-sm overflow-hidden font-mono text-[10px]">
		<div class="bg-gray-50 px-3 py-2 border-b border-border text-muted font-semibold">
			RECENT TRANSACTIONS
		</div>
		{#each [
			{ merchant: "Whole Foods Market", amount: "-$45.32", category: "Groceries", date: "Today" },
			{ merchant: "Shell Gas Station", amount: "-$52.00", category: "Transportation", date: "Yesterday" },
			{ merchant: "Netflix", amount: "-$15.99", category: "Entertainment", date: "Jan 15" },
			{ merchant: "Salary Deposit", amount: "+$3,250.00", category: "Income", date: "Jan 15" }
		] as txn}
			<div class="px-3 py-3 border-b border-border/50 flex justify-between items-center hover:bg-gray-50">
				<div class="flex-1">
					<div class="font-semibold text-foreground mb-1">{txn.merchant}</div>
					<div class="text-muted text-[9px]">{txn.category} • {txn.date}</div>
				</div>
				<div class="font-semibold {txn.amount.startsWith('+') ? 'text-green-600' : 'text-foreground'}">
					{txn.amount}
				</div>
			</div>
		{/each}
	</div>
</FeatureBlock>

<!-- Block 3: Identity Verification -->
<FeatureBlock 
	title="Identity Verification" 
	description="Verify account ownership and reduce fraud with instant bank account authentication and identity data."
	buttons={[
		{ text: "EXPLORE IDENTITY", icon: true }
	]}
>
	<div class="w-full h-full bg-white border border-border rounded shadow-sm p-6 font-mono text-xs">
		<div class="border-b border-border pb-3 mb-4">
			<div class="text-muted text-[10px] mb-2">IDENTITY VERIFICATION</div>
			<div class="flex items-center gap-2">
				<div class="w-8 h-8 bg-gradient-to-br from-accent/20 to-accent/10 rounded-full flex items-center justify-center font-bold">
					JD
				</div>
				<div>
					<div class="font-semibold">John Doe</div>
					<div class="text-[10px] text-muted">john.doe@email.com</div>
				</div>
			</div>
		</div>
		<div class="space-y-3">
			<div class="flex justify-between items-center text-[10px]">
				<span class="text-muted">Account Owner</span>
				<span class="text-green-600 flex items-center gap-1">
					<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M2 6L5 9L10 3" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
					</svg>
					Verified
				</span>
			</div>
			<div class="flex justify-between items-center text-[10px]">
				<span class="text-muted">Phone Number</span>
				<span class="text-green-600 flex items-center gap-1">
					<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M2 6L5 9L10 3" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
					</svg>
					Verified
				</span>
			</div>
			<div class="flex justify-between items-center text-[10px]">
				<span class="text-muted">Address</span>
				<span class="text-green-600 flex items-center gap-1">
					<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M2 6L5 9L10 3" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
					</svg>
					Verified
				</span>
			</div>
		</div>
	</div>
</FeatureBlock>

<!-- Block 4: Auth & Balance -->
<FeatureBlock 
	title="Auth & Balance" 
	description="Instantly verify bank accounts and retrieve real-time balance information for seamless account validation."
	buttons={[
		{ text: "VIEW AUTH API", icon: true }
	]}
	alignRight={true}
>
	<div class="w-full h-full bg-white border border-border rounded shadow-sm p-6 font-mono text-xs">
		<div class="border-b border-border pb-3 mb-4">
			<div class="text-muted text-[10px] mb-2">CONNECTED ACCOUNTS</div>
		</div>
		<div class="space-y-4">
			{#each [
				{ name: "Chase Checking", type: "Checking", balance: "$12,450.32", account: "****4532" },
				{ name: "Savings Account", type: "Savings", balance: "$45,230.00", account: "****7821" }
			] as account}
				<div class="border border-border rounded p-3">
					<div class="flex justify-between items-start mb-2">
						<div>
							<div class="font-semibold text-[11px]">{account.name}</div>
							<div class="text-muted text-[9px]">{account.type} • {account.account}</div>
						</div>
						<div class="text-green-600 text-[9px] bg-green-50 px-2 py-0.5 rounded">ACTIVE</div>
					</div>
					<div class="text-lg font-bold">{account.balance}</div>
				</div>
			{/each}
		</div>
	</div>
</FeatureBlock>

<!-- Block 5: Assets -->
<FeatureBlock 
	title="Assets" 
	description="Access comprehensive asset and liability data for underwriting, wealth management, and financial planning."
	buttons={[
		{ text: "EXPLORE ASSETS", icon: true }
	]}
>
	<div class="w-full h-full bg-white border border-border rounded shadow-sm p-6 font-mono text-xs">
		<div class="border-b border-border pb-3 mb-4">
			<div class="text-muted text-[10px] mb-2">ASSET OVERVIEW</div>
			<div class="text-2xl font-bold">$284,680.32</div>
			<div class="text-[10px] text-green-600 mt-1">+2.4% this month</div>
		</div>
		<div class="space-y-3">
			{#each [
				{ type: "Investment Account", value: "$156,230.00", percentage: "55%" },
				{ type: "Checking & Savings", value: "$57,680.32", percentage: "20%" },
				{ type: "Retirement (401k)", value: "$70,770.00", percentage: "25%" }
			] as asset}
				<div class="flex justify-between items-center">
					<div>
						<div class="text-[10px] font-semibold">{asset.type}</div>
						<div class="text-[9px] text-muted">{asset.percentage} of total</div>
					</div>
					<div class="font-semibold">{asset.value}</div>
				</div>
			{/each}
		</div>
	</div>
</FeatureBlock>
