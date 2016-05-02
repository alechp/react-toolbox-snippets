#RAW
Raw component source exported from http://react-toolbox.com/#/components


------------
APPBAR
------------
import AppBar from 'react-toolbox/lib/app_bar';

const AppBarTest = () => (
  <AppBar fixed flat>
    <a href='/home'>React Toolbox Docs</a>
    <Navigation />
  </AppBar>
);

------------
AUTOCOMPLETE
------------

import Autocomplete from 'react-toolbox/lib/autocomplete';

const source = {
  'ES-es': 'Spain',
  'TH-th': 'Thailand',
  'EN-gb': 'England',
  'EN-en': 'USA'
};

class AutocompleteTest extends React.Component {
  state = {
    countries: ['ES-es', 'TH-th']
  }

  handleChange = (value) => {
    this.setState({countries: value});
  };

  render () {
    return (
      <Autocomplete
        direction='down'
        selectedPosition='above'
        label='Choose countries'
        onChange={this.handleChange}
        source={source}
        value={this.state.countries}
      />
    );
  }
}

------------
AVATAR
------------

import Avatar from 'react-toolbox/lib/avatar';

const GithubIcon = () => (
  <svg viewBox='0 0 284 277'>
    <g><path d='M141.888675,0.0234927555 C63.5359948,0.0234927555 0,63.5477395 0,141.912168 C0,204.6023 40.6554239,257.788232 97.0321356,276.549924 C104.12328,277.86336 106.726656,273.471926 106.726656,269.724287 C106.726656,266.340838 106.595077,255.16371 106.533987,243.307542 C67.0604204,251.890693 58.7310279,226.56652 58.7310279,226.56652 C52.2766299,210.166193 42.9768456,205.805304 42.9768456,205.805304 C30.1032937,196.998939 43.9472374,197.17986 43.9472374,197.17986 C58.1953153,198.180797 65.6976425,211.801527 65.6976425,211.801527 C78.35268,233.493192 98.8906827,227.222064 106.987463,223.596605 C108.260955,214.426049 111.938106,208.166669 115.995895,204.623447 C84.4804813,201.035582 51.3508808,188.869264 51.3508808,134.501475 C51.3508808,119.01045 56.8936274,106.353063 65.9701981,96.4165325 C64.4969882,92.842765 59.6403297,78.411417 67.3447241,58.8673023 C67.3447241,58.8673023 79.2596322,55.0538738 106.374213,73.4114319 C117.692318,70.2676443 129.83044,68.6910512 141.888675,68.63701 C153.94691,68.6910512 166.09443,70.2676443 177.433682,73.4114319 C204.515368,55.0538738 216.413829,58.8673023 216.413829,58.8673023 C224.13702,78.411417 219.278012,92.842765 217.804802,96.4165325 C226.902519,106.353063 232.407672,119.01045 232.407672,134.501475 C232.407672,188.998493 199.214632,200.997988 167.619331,204.510665 C172.708602,208.913848 177.243363,217.54869 177.243363,230.786433 C177.243363,249.771339 177.078889,265.050898 177.078889,269.724287 C177.078889,273.500121 179.632923,277.92445 186.825101,276.531127 C243.171268,257.748288 283.775,204.581154 283.775,141.912168 C283.775,63.5477395 220.248404,0.0234927555 141.888675,0.0234927555' /></g>
  </svg>
);

const AvatarTest = () => (
  <div>
    <Avatar style={{backgroundColor: 'deepskyblue'}} icon='folder' />
    <Avatar icon={<GithubIcon />}/>
    <Avatar><img src='https://placeimg.com/80/80/animals'/></Avatar>
    <Avatar title='Javier' image='https://placeimg.com/80/80/animals'/>
    <Avatar style={{backgroundColor: 'yellowgreen'}}><GithubIcon /></Avatar>
  </div>
);

------------
BUTTON
------------

import {Button, IconButton} from 'react-toolbox/lib/button';

const GithubIcon = () => (
  <svg viewBox='0 0 284 277'>
    <g><path d='M141.888675,0.0234927555 C63.5359948,0.0234927555 0,63.5477395 0,141.912168 C0,204.6023 40.6554239,257.788232 97.0321356,276.549924 C104.12328,277.86336 106.726656,273.471926 106.726656,269.724287 C106.726656,266.340838 106.595077,255.16371 106.533987,243.307542 C67.0604204,251.890693 58.7310279,226.56652 58.7310279,226.56652 C52.2766299,210.166193 42.9768456,205.805304 42.9768456,205.805304 C30.1032937,196.998939 43.9472374,197.17986 43.9472374,197.17986 C58.1953153,198.180797 65.6976425,211.801527 65.6976425,211.801527 C78.35268,233.493192 98.8906827,227.222064 106.987463,223.596605 C108.260955,214.426049 111.938106,208.166669 115.995895,204.623447 C84.4804813,201.035582 51.3508808,188.869264 51.3508808,134.501475 C51.3508808,119.01045 56.8936274,106.353063 65.9701981,96.4165325 C64.4969882,92.842765 59.6403297,78.411417 67.3447241,58.8673023 C67.3447241,58.8673023 79.2596322,55.0538738 106.374213,73.4114319 C117.692318,70.2676443 129.83044,68.6910512 141.888675,68.63701 C153.94691,68.6910512 166.09443,70.2676443 177.433682,73.4114319 C204.515368,55.0538738 216.413829,58.8673023 216.413829,58.8673023 C224.13702,78.411417 219.278012,92.842765 217.804802,96.4165325 C226.902519,106.353063 232.407672,119.01045 232.407672,134.501475 C232.407672,188.998493 199.214632,200.997988 167.619331,204.510665 C172.708602,208.913848 177.243363,217.54869 177.243363,230.786433 C177.243363,249.771339 177.078889,265.050898 177.078889,269.724287 C177.078889,273.500121 179.632923,277.92445 186.825101,276.531127 C243.171268,257.748288 283.775,204.581154 283.775,141.912168 C283.775,63.5477395 220.248404,0.0234927555 141.888675,0.0234927555' /></g>
  </svg>
);

const TestButtons = () => (
  <div>
    <Button href='http://github.com/javivelasco' target='_blank' raised>
      <GithubIcon /> Github
    </Button>
    <Button icon='bookmark' label='Bookmark' accent />
    <Button icon='bookmark' label='Bookmark' raised primary />
    <Button icon='inbox' label='Inbox' flat />
    <Button icon='add' floating />
    <Button icon='add' floating accent mini />
    <IconButton icon='favorite' accent />
    <IconButton primary><GithubIcon /></IconButton>
    <Button icon='add' label='Add this' flat primary />
    <Button icon='add' label='Add this' flat disabled />
  </div>
);


------------
CARD
------------

import { Card, CardMedia, CardTitle, CardText, CardActions } from 'react-toolbox/lib/card';

const dummyText = 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.';

const TestCards = () => (
  <Card style={{width: '350px'}}>
    <CardTitle
      avatar='https://placeimg.com/80/80/animals'
      title='Avatar style title'
      subtitle='Subtitle here'
    />
    <CardMedia
      aspectRatio='wide'
      image='https://placeimg.com/800/450/nature'
    />
    <CardTitle
      title='Title goes here'
      subtitle='Subtitle here'
    />
    <CardText>{dummyText}</CardText>
    <CardActions>
      <Button label='Action 1' />
      <Button label='Action 2' />
    </CardActions>
  </Card>
);

return <TestCards />;


------------
CHIP
------------


import Avatar from 'react-toolbox/lib/avatar';
import Chip from 'react-toolbox/lib/chip';

const ChipTest = () => (
  <div>
    <Chip>Example chip</Chip>
    <Chip>
      <span style={{textDecoration: 'line-through'}}>Standard</span>
      <strong>Custom</strong> chip <small>(custom markup)</small>
    </Chip>

    <Chip deletable>Deletable Chip</Chip>

    <Chip>
      <Avatar style={{backgroundColor: 'deepskyblue'}} icon='folder' />
      <span>Avatar Chip</span>
    </Chip>

    <Chip>
      <Avatar title='A' /><span>Initial chip</span>
    </Chip>

    <Chip>
      <Avatar><img src='https://placeimg.com/80/80/animals'/></Avatar>
      <span>Image contact chip</span>
    </Chip>
  </div>
);


------------
CHECKBOX
------------

import Checkbox from 'react-toolbox/lib/checkbox';

class TestCheckbox extends React.Component {
  state = { check1: true, check2: false };

  handleChange = (field, value) => {
    this.setState({...this.state, [field]: value});
  };

  render () {
    return (
      <div>
        <Checkbox
          checked={this.state.check1}
          label='Checked option'
          onChange={this.handleChange.bind(this, 'check1')}
        />
        <Checkbox
          checked={this.state.check2}
          label='Unchecked option'
          onChange={this.handleChange.bind(this, 'check2')}
        />
        <Checkbox
          checked
          disabled
          label='Disabled checkbox'
        />
      </div>
    );
  }
}


------------
DATE PICKER
------------

import DatePicker from 'react-toolbox/lib/date_picker';

const datetime = new Date(2015, 10, 16);
const min_datetime = new Date(new Date(datetime).setDate(8));
datetime.setHours(17);
datetime.setMinutes(28);

class DatePickerTest extends React.Component {
  state = {date2: datetime};

  handleChange = (item, value) => {
    this.setState({...this.state, [item]: value});
  };

  render () {
    return (
      <section>
        <DatePicker label='Birthdate' onChange={this.handleChange.bind(this, 'date1')} value={this.state.date1} />
        <DatePicker label='Expiration date' minDate={min_datetime} onChange={this.handleChange.bind(this, 'date2')} value={this.state.date2} />
        <DatePicker label='Formatted date' inputFormat={(value) => `${value.getDate()}/${value.getMonth()}/${value.getFullYear()}`} onChange={this.handleChange.bind(this, 'date3')} value={this.state.date3} />
      </section>
    );
  }
}

------------
DIALOG
------------

import Dialog from 'react-toolbox/lib/dialog';

class DialogTest extends React.Component {
  state = { 
    active: false 
  };

  handleToggle = () => {
    this.setState({active: !this.state.active});
  }

  actions = [
    { label: 'Cancel', onClick: this.handleToggle },
    { label: 'Save', onClick: this.handleToggle }
  ];

  render () {
    return (
      <div>
        <Button label='Show my dialog' onClick={this.handleToggle} />
        <Dialog
          actions={this.actions}
          active={this.state.active}
          onEscKeyDown={this.handleToggle}
          onOverlayClick={this.handleToggle}
          title='My awesome dialog'
        >
          <p>Here you can add arbitrary content. Components like Pickers are using dialogs now.</p>
        </Dialog>
      </div>
    );
  }
}


------------
DRAWER
------------

import Drawer from 'react-toolbox/lib/drawer';

class DrawerTest extends React.Component {
  state = {
    active: false
  };

  handleToggle = () => {
    this.setState({active: !this.state.active});
  };

  render () {
    return (
      <div>
        <Button label='Show Drawer' raised accent onClick={this.handleToggle} />
        <Drawer active={this.state.active} onOverlayClick={this.handleToggle}>
          <h5>This is your Drawer.</h5>
          <p>You can embed any content you want, for example a Menu.</p>
        </Drawer>
      </div>
    );
  }
}


------------
DROPDOWN
------------

import Dropdown from 'react-toolbox/lib/dropdown';

const countries = [
  { value: 'EN-gb', label: 'England' },
  { value: 'ES-es', label: 'Spain'},
  { value: 'TH-th', label: 'Thailand' },
  { value: 'EN-en', label: 'USA'}
];

class DropdownTest extends React.Component {
  state = {
    value: 'ES-es',
  };

  handleChange = (value) => {
    this.setState({value: value});
  };

  render () {
    return (
      <Dropdown
        auto
        onChange={this.handleChange}
        source={countries}
        value={this.state.value}
      />
    );
  }
}


------------
FONT ICON
------------

import FontIcon from 'react-toolbox/lib/font_icon';

const FontIcons = () => (
  <span>
    <FontIcon value='add' />
    <FontIcon value='favorite' />
    <FontIcon>star</FontIcon>
  </span>
);


------------
INPUT
------------

import Input from 'react-toolbox/lib/input';

class InputTest extends React.Component {
  state = { name: '', phone: '', email: '', hint: '' };

  handleChange = (name, value) => {
    this.setState({...this.state, [name]: value});
  };

  render () {
    return (
      <section>
        <Input type='text' label='Name' name='name' value={this.state.name} onChange={this.handleChange.bind(this, 'name')} maxLength={16 } />
        <Input type='text' label='Disabled field' disabled />
        <Input type='email' label='Email address' icon='email' value={this.state.email} onChange={this.handleChange.bind(this, 'email')} />
        <Input type='tel' label='Phone' name='phone' icon='phone' value={this.state.phone} onChange={this.handleChange.bind(this, 'phone')} />
        <Input type='text' value={this.state.hint} label='Required Field' hint='With Hint' required onChange={this.handleChange.bind(this, 'hint')} icon={<span>J</span>} />
      </section>
    );
  }
}


------------
LAYOUT
------------

import { AppBar, Checkbox, IconButton } from 'react-toolbox';
import { Layout, NavDrawer, Panel, Sidebar } from 'react-toolbox';

class LayoutTest extends React.Component {
    state = {
        drawerActive: false,
        drawerPinned: false,
        sidebarPinned: false
    };

    toggleDrawerActive = () => {
        this.setState({ drawerActive: !this.state.drawerActive });
    };

    toggleDrawerPinned = () => {
        this.setState({ drawerPinned: !this.state.drawerPinned });
    }

    toggleSidebar = () => {
        this.setState({ sidebarPinned: !this.state.sidebarPinned });
    };

    render() {
        return (
            <Layout>
                <NavDrawer active={this.state.drawerActive}
                    pinned={this.state.drawerPinned} permanentAt='xxxl'
                    onOverlayClick={ this.toggleDrawerActive }>
                    <p>
                        Navigation, account switcher, etc. go here.
                    </p>
                </NavDrawer>
                <Panel>
                    <AppBar><IconButton icon='menu' inverse={ true } onClick={ this.toggleDrawerActive }/></AppBar>
                    <div style={{ flex: 1, overflowY: 'auto', padding: '1.8rem' }}>
                        <h1>Main Content</h1>
                        <p>Main content goes here.</p>
                        <Checkbox label='Pin drawer' checked={this.state.drawerPinned} onChange={this.toggleDrawerPinned} />
                        <Checkbox label='Show sidebar' checked={this.state.sidebarPinned} onChange={this.toggleSidebar} />
                    </div>
                </Panel>
                <Sidebar pinned={ this.state.sidebarPinned } width={ 5 }>
                    <div><IconButton icon='close' onClick={ this.toggleSidebar }/></div>
                    <div style={{ flex: 1 }}>
                        <p>Supplemental content goes here.</p>
                    </div>
                </Sidebar>
            </Layout>
        );
    }
}


------------
LINK
------------

import Link from 'react-toolbox/lib/link';

const LinksTest = () => (
  <nav>
    <Link active href='/#/components/link' label='Work' count={4} icon='business' />
    <Link href='/#/components/link' label='Blog' icon='speaker_notes' />
    <Link href='/#/components/link' label='Explore' icon='explore' />
  </nav>
);



------------
LIST
------------

import { List, ListItem, ListSubHeader, ListDivider, ListCheckbox } from 'react-toolbox/lib/list';

const ListTest = () => (
  <List selectable ripple>
    <ListSubHeader caption='Explore characters' />
    <ListItem
      avatar='https://dl.dropboxusercontent.com/u/2247264/assets/m.jpg'
      caption='Dr. Manhattan'
      legend='Jonathan 'Jon' Osterman'
      rightIcon='star'
    />
    <ListItem
      avatar='https://dl.dropboxusercontent.com/u/2247264/assets/o.jpg'
      caption='Ozymandias'
      legend='Adrian Veidt'
      rightIcon='star'
    />
    <ListItem
      avatar='https://dl.dropboxusercontent.com/u/2247264/assets/r.jpg'
      caption='Rorschach'
      legend='Walter Joseph Kovacs'
      rightIcon='star'
    />
    <ListSubHeader caption='Configuration' />
    <ListCheckbox checked caption='Notify new comics' legend='You will receive a notification when a new one is published' />
    <ListDivider />
    <ListItem caption='Contact the publisher' leftIcon='send' />
    <ListItem caption='Remove this publication' leftIcon='delete' />
  </List>
);


------------
MENU
------------

import {IconMenu, MenuItem, MenuDivider } from 'react-toolbox/lib/menu';

const MenuTest = () => (
  <IconMenu icon='more_vert' position='top-left' menuRipple>
    <MenuItem value='download' icon='get_app' caption='Download' />
    <MenuItem value='help' icon='favorite' caption='Favorite' />
    <MenuItem value='settings' icon='open_in_browser' caption='Open in app' />
    <MenuDivider />
    <MenuItem value='signout' icon='delete' caption='Delete' disabled />
  </IconMenu>
);


------------
NAVIGATION
------------

import Navigation from 'react-toolbox/lib/navigation';
import Link from 'react-toolbox/lib/link';

const actions = [
  { label: 'Alarm', raised: true, icon: 'access_alarm'},
  { label: 'Location', raised: true, accent: true, icon: 'room'}
];

const NavigationTest = () => (
  <div>
    <Navigation type='horizontal' actions={actions} />
    <Navigation type='vertical'>
      <Link href='http://' label='Inbox' icon='inbox' />
      <Link href='http://' active label='Profile' icon='person' />
    </Navigation>
  </div>
);


------------
PROGRESS BAR
------------

import ProgressBar from 'react-toolbox/lib/progress_bar';

const ProgressTest = () => (
  <div>
    <ProgressBar type='circular' mode='indeterminate' />
    <ProgressBar type='linear' mode='determinate' value={83} buffer={90}/>
  </div>
);


------------
RADIO BUTTONS
------------

import { RadioGroup, RadioButton } from 'react-toolbox/lib/radio';

class RadioTest extends React.Component {
  state = {
    value: 'vvendetta'
  };

  handleChange = (value) => {
    this.setState({value});
  };

  render () {
    return (
      <RadioGroup name='comic' value={this.state.value} onChange={this.handleChange}>
        <RadioButton label='The Walking Dead' value='thewalkingdead'/>
        <RadioButton label='From Hell' value='fromhell' disabled/>
        <RadioButton label='V for a Vendetta' value='vvendetta'/>
        <RadioButton label='Watchmen' value='watchmen'/>
      </RadioGroup>
    );
  }
}

------------
RIPPLE
------------

import Ripple from 'react-toolbox/lib/ripple';

const Link = (props) => (
  <a {...props} style={{position: 'relative'}}>
    {props.children}
  </a>
);

const RippleLink = Ripple({spread: 3})(Link);
const RippleTest = () => <RippleLink href='#'>Test</RippleLink>;



------------
SLIDER
------------

import Slider from 'react-toolbox/lib/slider';

class SliderTest extends React.Component {
  state = {
    slider2: 5,
    slider3: 1
  };

  handleChange = (slider, value) => {
    const newState = {};
    newState[slider] = value;
    this.setState(newState);
  };

  render () {
    return (
      <section>
        <p>Normal slider</p>
        <Slider value={this.state.slider1} onChange={this.handleChange.bind(this, 'slider1')} />
        <p>With steps, initial value and editable</p>
        <Slider min={0} max={10} editable value={this.state.slider2} onChange={this.handleChange.bind(this, 'slider2')} />
        <p>Pinned and with snaps</p>
        <Slider pinned snaps min={0} max={10} step={1} editable value={this.state.slider3} onChange={this.handleChange.bind(this, 'slider3')} />
      </section>
    );
  }
}



------------
SNACKBAR
------------

import { Button, Snackbar } from 'react-toolbox';

class SnackbarTest extends React.Component {
  handleClick = () => {
    this.refs.snackbar.show();
  };

  handleSnackbarClick = () => {
    this.refs.snackbar.hide();
  };

  render () {
    return (
      <section>
        <Button label='Show Snackbar' raised onClick={this.handleClick} />
        <Snackbar
          action='Nice'
          icon='question_answer'
          label='A new developer started using React Toolbox'
          onClick={this.handleSnackbarClick}
          ref='snackbar'
          type='accept'
      />
      </section>
    );
  }
}



------------
SWITCH
------------

import Switch from 'react-toolbox/lib/switch';

class SwitchTest extends React.Component {
  state = {
    switch_1: true,
    switch_2: false,
    switch_3: true
  };

  handleChange = (field, value) => {
    this.setState({...this.state, [field]: value});
  };

  render () {
    return (
      <section>
        <Switch
          checked={this.state.switch_1}
          label='Push notifications'
          onChange={this.handleChange.bind(this, 'switch_1')}
        />
        <Switch
          checked={this.state.switch_2}
          label='Mail notifications'
          onChange={this.handleChange.bind(this, 'switch_2')}
        />
        <Switch
          checked={this.state.switch_3}
          disabled
          label='Nothing, thanks'
          onChange={this.handleChange.bind(this, 'switch_3')}
        />
      </section>
    );
  }
}




------------
TABLE
------------

import Table from 'react-toolbox/lib/table';

const UserModel = {
  name: {type: String},
  twitter: {type: String},
  birthdate: {type: Date},
  cats: {type: Number},
  dogs: {type: Number},
  active: {type: Boolean}
};

const users = [
  {name: 'Javi Jimenez', twitter: '@soyjavi', birthdate: new Date(1980, 3, 11), cats: 1},
  {name: 'Javi Velasco', twitter: '@javivelasco', birthdate: new Date(1987, 1, 1), dogs: 1, active: true}
];

class TableTest extends React.Component {
  state = { selected: [], source: users };

  handleChange = (row, key, value) => {
    const source = this.state.source;
    source[row][key] = value;
    this.setState({source});
  };

  handleSelect = (selected) => {
    this.setState({selected});
  };

  render () {
    return (
      <Table
        model={UserModel}
        onChange={this.handleChange}
        onSelect={this.handleSelect}
        selectable
        selected={this.state.selected}
        source={this.state.source}
      />
    );
  }
}



------------
TABS
------------

import {Tab, Tabs} from 'react-toolbox';

class TabsTest extends React.Component {
  state = {
    index: 1
  };

  handleTabChange = (index) => {
    this.setState({index});
  };

  handleActive = () => {
    console.log('Special one activated');
  };

  render () {
    return (
      <Tabs index={this.state.index} onChange={this.handleTabChange}>
        <Tab label='Primary'><small>Primary content</small></Tab>
        <Tab label='Secondary' onActive={this.handleActive}><small>Secondary content</small></Tab>
        <Tab label='Third' disabled><small>Disabled content</small></Tab>
        <Tab label='Fourth' hidden><small>Fourth content hidden</small></Tab>
        <Tab label='Fifth'><small>Fifth content</small></Tab>
      </Tabs>
    );
  }
}



------------
TOOLTIP
------------

import Button from 'react-toolbox/lib/button';
import Tooltip from 'react-toolbox/lib/tooltip';
import Link from 'react-toolbox/lib/link';

const TooltipButton = Tooltip(Button);
const TooltipInput = Tooltip(Input);
const TooltipLink = Tooltip(Link);

const TooltipTest = () => (
  <div>
    <TooltipButton label='Bookmark' icon='bookmark' raised primary tooltip='Bookmark Tooltip' tooltipDelay={1000} />
    <TooltipButton icon='add' floating accent tooltip='Floating Tooltip' />
    <TooltipLink count={42} href='#' label='The answer is' icon='speaker_notes' tooltip='Question - universe?'/>
    <TooltipInput tooltip='lorem ipsum...' />
  </div>
);



------------
TIME PICKER
------------

import TimePicker from 'react-toolbox/lib/time_picker';
let time = new Date();
time.setHours(17);
time.setMinutes(28);

class TimePickerTest extends React.Component {
    state = {time};

  handleChange = (time) => {
      this.setState({time});
  };

  render () {
      return <TimePicker label='Finishing time' onChange={this.handleChange} value={this.state.time} />;
  }
}
