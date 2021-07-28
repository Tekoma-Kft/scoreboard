<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Kpi from "./Kpi.svelte";
</script>

<Meta
  title="Example/Kpi"
  component={Kpi}
  argTypes={{
    onClick: { action: "onClick" },
  }}
/>

<Template let:args>
  <Kpi {...args} on:click={args.onClick} />
</Template>

<Story
  name="Primary"
  args={{
    primary: true,
  }}
/>
